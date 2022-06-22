# Usage on building out content

This document will contain information on common things you might do when creating new content and doing translations.

## Creating a news post
The content folder contains all the news posts. Go into the content > (your language) > posts > (current year) folder. From there you can create a new md file. An easy way is to duplicate an existing one. You can update the title and content as needed. If you are running the "hugo server", you should be able to preview it directly in your browser. 

## Marking a post or page as a draft so it isn't published/shown
On the top most section of your markdown file (called front matter in Hugo), add a variable with "draft: true"

## Adding images
Images in general are stored in the themes > krita-org-theme > static > images folder. There are two folders that are in here that are only for organizational purposes

1. pages - content that is not news specific
1. posts - news

To avoid naming conflicts, post images are currently broken apart into years. If you are creating a news story in 2022, you would put the images in the posts > 2022 folder.

# Adding YouTube videos and shortcodes
There are shortcuts (called shortcodes) that allow you to easily add more complex things to your markdown files. Here are few simple examples: 

{{< youtube spy-0EKBcvQ >}}

{{< tweet user="SanDiegoZoo" id="1453110110599868418" >}}

{{< vimeo 146022717 >}}


## Adding language specific images
While doing a translation, you might have an image that has text on it that needs to be translated. We generally try to avoid this, but it happens sometimes. After getting/creating a new localized image, put it directly in the posts area where you are creating your MD file for your language. You can create an 'images' folder in the posts folder and put it in there to be more organized. You can locally reference the image in a language by doing something like 'images/my-custom-image.png'. 


# Adding functionality outside of mark down files
Markdown is create, but it has limitations on what it can do and display. To get around this, you can create "shortcodes" in Hugo. This is a template that you create in HTML that you can access in an easy way from markdown. To see the existing custom shortodes, see the themes > krita-org-theme > layouts > shortcodes directory.



