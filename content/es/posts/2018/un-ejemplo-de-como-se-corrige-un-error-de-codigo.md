---
title: "Un ejemplo de como se corrige un error de código"
date: "2018-09-18"
categories: 
  - "uncategorized-es"
---

[El evento de recaudación de fondos para Krita en el 2018 se basa en la corrección de errores](https://krita.org). De hecho ya estamos adentrados en el trabajo, por lo que podemos darle un vistazo no muy técnico al proceso en el que Dmitry corrigió uno de estos "bichos" el dia de ayer. Este es el error reportado (en ingles): "[key sequence ctrl+w ambiguous with photoshop compatible bindings set](https://bugs.kde.org/show_bug.cgi?id=398729)", Y [ésto es como se ha corregido](https://phabricator.kde.org/R37:f2f2be209d8d40a5e7df97f6d259e14818355a4c).

De hecho  Dmitry y yo (Boudewijn) nos pusimos a revisar el mismo problema al mismo tiempo, el cual está relacionado con el uso de atajos de teclado, el cual se se usa para el cierre de ventanas, pero que al usarlo, una ventana se abre diciendo que el atajo es ambiguo y por lo tanto no se ejecuta ninguna acción.

[![](/images/posts/2018/ambiguous.png)](https://krita.org/wp-content/uploads/2018/09/ambiguous.png)

El dialogo no menciona cual es la otra acción que produce la ambigüedad, solo que existe, todo lo que produce un evento en Krita que se puede usar con un atajo del teclado es referido como una, [_acción_](http://doc.qt.io/qt-5/qaction.html). Y muy al fondo del código, Qt mantiene la lista de todos los atajos, Qt es una base externa  (creado por otra organización) que usamos pero que nosotros no modificamos directamente.

Por lo que revisamos el código de Krita, en éste, la acción para cerrar una imagen es la única que con ese atajo, pero ademas otro error que encontramos en Krita es el que por defecto, Krita no le asigna ninguna acción a este atajo. En Linux es simplemente Ctrl+W, en windows es COMMAND+W igual que en MacOS.

Lo curioso, que en el grupo de atajos de Photoshop (atajos predefinidos disponibles en Krita que se asemejan a los de éste programa) proporcionan al acción correcta en Krita. Por lo que si seleccionas [ese conjunto](https://docs.krita.org/en/reference_manual/preferences/shortcut_settings.html), el atajo se incorpora correctamente.

Lo mas interesante es que si no se elije ningún conjunto o perfil de atajos, lo que debería hacer que Krita no use ningún atajo para esa acción, aun así Krita usa el atajo de cualquier manera.

Por lo que eso solo significa una sola cosa: La acción para serrar la imagen en Krita está vacía, nunca se usa realmente. En alguna otra parte, fuera de el código de Krita, esta acción es creada.

Finalmente Dmitry comenzó a investigar el código de Qt directamente, del cual algunas partes son bastante antiguas, y precisamente una de estas partes que hace posible el usar pequeñas ventanas dentro de otras mas grandes es una de esas antigüedades.

/\*!
    \\internal
\*/
void QMdiSubWindowPrivate::createSystemMenu()
{
...
    addToSystemMenu(CloseAction, QMdiSubWindow::tr("&Close"), SLOT(close()));
...
    actions\[CloseAction\]->setShortcuts(QKeySequence::Close);
....
}
#endif

¡Ajá! Ahí es donde otra acción se crea, y donde se asigna el atajo, completamente fuera de Krita y de nuestro control. Éste error el cual fue reportado apenas hace dos días, ¡Ha estado presente en Krita desde la versión 2.9! (basado en el código que se ha usado), Por lo tanto, para corregir las cosas por nuestro lado, tenemos que cerciorarnos de que Krita asigne su propia acción a el atajo definido; Esto solo es posible cuando no permitimos que Qt produzca la acción a no ser que sea para el uso de un menú de una ventana de dialogo.

    /\*\*
     \* Qt has a weirdness, it has hardcoded shortcuts added to an action
     \* in the window menu. We need to reset the shortcuts for that menu
     \* to nothing, otherwise the shortcuts cannot be made configurable.
     \*
     \* See: https://bugs.kde.org/show\_bug.cgi?id=352205
     \*      https://bugs.kde.org/show\_bug.cgi?id=375524
     \*      https://bugs.kde.org/show\_bug.cgi?id=398729
     \*/
    QMdiSubWindow \*subWindow = d->mdiArea->currentSubWindow();
    if (subWindow) {
        QMenu \*menu = subWindow->systemMenu();
        if (menu) {
            Q\_FOREACH (QAction \*action, menu->actions()) {
                action->setShortcut(QKeySequence());
            }
        }
    }

Lo que significa que para cada ventana de dialogo que tenemos, coleccionamos el menú, en cada entrada de el menú, eliminamos el atajo de teclado. Así nuestro atajo general para cerrar una imagen siempre se usa por de facto, permitiendo ademas que nuestros usuarios puedan cambiarlo como gusten.
