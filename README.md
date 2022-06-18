# Krita.org website

Marketing website for the open source art application krita. Built with the Hugo static site generator

## Dependencies

- Hugo: Command line tool used to build project (https://gohugo.io/getting-started/installing/)

There is no installer for Hugo when you download it. The executable you download is a command line application. You will need to add executable location to your PATH environment variables. This will allow the computer to understand and use the hugo command line tool.

Run command to verify that hugo is installed when done
    hugo version


## Building and launching

Open the root location in something like Visual Studio Code, or just navigate via command line/terminal window. Type the following:

    hugo server

This will build and run the project under a localhost. The command line output will tell you the URL that is being used. Hugo also has a watch process, so changes that are done will be updated. The -D flag includes posts that are marked as drafts

## Adding or editing posts

Add a new MD file to the content > (lang) > posts area. See other markdown files for reference.

# Changing Templates/Layouts

If you go in the themes > krita-org-theme > layouts, you will notice there are a lot of template files there. This is a template that a page can use. If a page(MD file) is using a template, it will have a "type" variable set at the top. This maps directly to the folder in this layout area.

Template variable errors can be very cryptic to read when doing things like looping over content. Do small changes at a time to make it easier to know what went wrong.

Note: If you are running the project and make changes to the template, you might have to stop the server from running (I use Ctrl+C), then restart it again with 'hugo server' to see the changes.

# Adding tabs to groups of pages

Some website sections like the About area has multiple pages inside (History, About, Press, etc ). There are two parts to making this sub-navigation work
1. Adding a "group" variable to the top of each page that needs to be set to the section.
2. Having a template (type variable) that that shows and filters that data. Templates are in the theme > krita-org-theme > layouts folder



## Final production build

Run the command: 
    hugo

The files will be generated to the Public folder. You should be able to copy that to the web server.


# TODO items
1. Start filling out homepage with relevant information and translations
2. Start filling out features page with relevant information and translations
3. Start filling out download page with relevant information and translations

4. Think about design updates a bit
---- query some artists on Krita artist about using their artwork

5. Whenever the project gets a bit farther, get a plan on moving images/assets to an external location/server to reduce GIT repo size
--- Ben (KDE sys admin) says we can put heavier files all on cdn.kde.org. It has heavy caching, so be aware of that
--- if we have custom videos (not on YouTube), we can put those on cdn.kde.org too

# Questions before we go live
1. Not sure how we are going to get Mollie payments to the fund site if we shut down the WordPress site

