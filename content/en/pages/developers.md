---
title: "Developers"
date: "2018-05-13"
---

You'll be able to work on one of the coolest and fastest-growing open source painting programs out there.

Krita also benefits from a modular architecture and the use of the KDE Frameworks and Qt libraries, which makes it easier to focus on new features instead of reinventing the wheel. And it makes coding fun!  To work on Krita, you have to use C++ and Qt. It's a good way to learn both, actually!

### Getting Started

1. Most important: [https://phabricator.kde.org/source/krita/](https://phabricator.kde.org/source/krita/). There is a mirror on [Github](https://github.com/KDE/krita). Note that we do not use Github for development, don't create pull requests or file issues on github.
2. [KDE Developer](https://community.kde.org/Getinvolved/development) wiki
3. Set up your development environment and [build Krita](https://docs.krita.org/en/untranslatable_pages/building_krita.html).
4. Find a few bugs to fix in [KDE's Bugtracking system](https://bugs.kde.org/). It's often a good idea to get some experience with the code through fixing bugs, to get familiar with the development process without being overwhelmed. Though there's nothing against working on that cool feature that scratches your itch!
5. For bugs, it's a good idea to start with "Junior Jobs." These are a set of relatively easy tasks for new developers. In the Bugtracking system, [these are the bugs marked with "JJ.](https://bugs.kde.org/buglist.cgi?bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&keywords=junior-jobs%2C%20&keywords_type=allwords&list_id=1537004&product=krita&query_format=advanced)"

  

### Working with the Krita Code Base

**Architecture** - The code base changes all the time with Krita, we're not afraid of big refactorings, so there is no up to date documentation on the code architecture. There have been some written in the past, but they quickly became outdated and of little use. There is a fairly up to date [API guide](https://api.kde.org/extragear-api/graphics-apidocs/krita/html/index.html) if you want to look at how the code is structured.

**Integrated Development Environment (IDE)** - The most popular IDEs that we use are Qt Creator, Emacs, KDevelop, or vim. Qt Creator has the advantage of the ctrl-k menu, which lets you leap to classes, lines, everywhere. You don't have to build with Qt Creator though! It can be easier to jump to the terminal, do a 'make', check what's up, and then jump back to the IDE.

**Debugging -** There are large and small problems. For small problems the debugger in Qt Creator (run external application) or adding qDebug messages to the code is fine. If the problem is difficult, the first step should always be to write a unit test. A small bit of code that follows a set pattern and exercises the faulty code and shows the problem. That helps so much figuring out a fix and keeping it fixed.

**Resources -** The most important step to learning the code is to really understand memory management: pointers, smart pointers and pointer arithmetic. This is something that Java and C# developers  will need to spend a little more time understanding. Here are a couple resources to get you more familiar with C++ and Qt.

- [Qt Concepts](http://qt-project.org/doc/qt-4.8/how-to-learn-qt.html)
- [Design Patterns with Qt](http://www.ics.com/designpatterns/book/index.html)
- C++ in a Nutshell by O'Reilly (book)

### Tips when Tackling Issues

**Features and Refactorings** - Sometimes you just know that a lot of work is going to be needed to reach a particular goal. These will go in separate feature branches off 'master'.

**Performance Improvements** - Sometimes you don't feel like working on a feature - or someone mentioned something being particularly slow. The first thing to do then is carry out that scenario when Krita runs under [callgrind](http://c.learncodethehardway.org/book/ex41.html) and [vtune](http://en.wikipedia.org/wiki/VTune). These tools show bottlenecks at the end of a run. It's important to use both, since both give different insights!

**Bugs** - Sometimes you rummage around the bugs on b.k.o to see what looks like a nice Saturday morning fix. Sometimes a bug is really urgent (like all data loss bugs). Sometimes someone on IRC or the forum mentions a bug. The first thing to do is reproduce it. The second thing is to look in the code to see what is going on. If it's a crash bug, especially one that seems mysterious, it might help to google for a few of the key lines in the backtrace. Sometimes it's a distribution issue!

**Blockers** - If you are helping with Krita and your progress is being blocked by something - let us know! Talk with us on the [Krita IRC channel](https://krita.org/irc/) and we will see what we can do to help!

### Get in touch and become a developer

If you're working on a bug fix, or maybe a bit of GUI polish, you might get stumped. The best thing to do then is to get in touch with the rest of the Krita team. Part of the fun of working on an open source application is the community, after all! Join us on [#krita on irc.freenode.net](https://krita.org/irc/) (keep in mind that most people are in Europe or India) and just ask your question. Stay around, especially if you don't get an answer immediately. Some of the developers have their irc client open permanently and will often answer questions hours later!

You can also send mail to the mailinglist: [kimageshop@kde.org](https://mail.kde.org/mailman/listinfo/kimageshop). It's better not to send mail to individual developers directly, you might accidentally pick someone who hasn't got the answer, and miss the chance of getting your question answered by another Krita developer.

When you've made your first patch, post it to [https://phabricator.kde.org/](https://phabricator.kde.org/). Look at the [documentation on how to submit your patch](https://techbase.kde.org/Development/Phabricator). The developers will check your patch and if it's okay push it to git for you. After the third patch, you'll be asked to upgrade your KDE identity account to developer status! Follow this guide: [https://techbase.kde.org/Contribute/Get\_a\_Contributor\_Account](https://community.kde.org/Infrastructure/Get_a_Developer_Account).

An easy way to create a patch is to make all of your commits in a local GIT branch and run this in the terminal :

git diff HEAD~2..HEAD > my-patch.diff

This will make a diff (text file) of the last 2 commits that you have done. Attach the diff for review.

### Commit Access

After you make a few patches, you will have the privelege of pushing patches directly to the code base. Before you can do that, you will need to switch your git repository from a read only version to a read/write version. The git command looks like this to switch.

git remote set-url origin git@git.kde.org:krita

You will also need to have SSH access setup and a KDE identity account. You can read more about that here...

[Getting a developer account](https://community.kde.org/Infrastructure/Get_a_Developer_Account)
