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
0. Make sure language codes mirror docs.krita.org. This makes it easier to bounce to the docs site while retaining the same language

1. Since this is a static site, it has no logic with when to display a 404 page. That will have to be configured on the server whenever we start testing it out
- For testing locally, you should be able to go to your /404.html (mine is http://localhost:1313/404.html)

2. Make a site map page so it is more discoverable for people to see all the cotent that exists for the website
- This will be useful for testing and cleaning up data/pages


# Questions before we go live
1. Not sure how we are going to get Mollie payments to the fund site if we shut down the WordPress site. it sounds like Mollie might not be the best solution for single time payments, so look into alternatives


