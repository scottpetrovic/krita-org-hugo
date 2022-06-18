# Krita.org website

Marketing website for the open source art application krita

## Dependencies

- Hugo: Command line tool used to build project (https://gohugo.io/getting-started/installing/)
-- run "hugo version" after installation in the terminal/command line. It should show a version number if installed

## Building and launching

Open the root location in something like Visual Studio Code, or just navigate via command line/terminal window. Type the following:

    hugo server -D

This will build and run the project under a localhost. Hugo also has a watch process, so changes that are done will be updated. The -D flag includes posts that are marked as drafts

## Adding or editing posts

Add a new MD file to the content > posts area. See other markdown files for reference.

# Changing Templates/Layouts

If you go in the themes > blog-theme > layouts, you will notice there are a lot of template files there. This is a template that a page can use. If a page(MD file) is using a template, it will have a "type" variable set at the top. This maps directly to the folder in this layout area.

Template variable errors can be very cryptic to read when doing things like looping over content. Do small changes at a time to make it easier to know what went wrong.

Note: If you are running the project and make changes to the template, you might have to stop the server from running (I use Ctrl+C), then restart it again with 'hugo server'

# Adding tabs to groups of pages

Some website sections like the About area has multiple pages inside (History, About, Press, etc ). There are two parts to making this sub-navigation work
1. Adding a "group" variable to the top of each page that needs to be set to the section.
2. Having a template (type variable) that that shows and filters that data.

As an example going back to the About us section. 

## Final production build

Run the command: 
    hugo

The files will be generated to the Public folder. You should be able to copy that to the web server.


# TODOS
1. Not sure how we are going to get Mollie payments to the fund site if we shut down the WordPress site
2. Possible to consolidate template files with baseof or default file?
3. change theme to krita-org-theme