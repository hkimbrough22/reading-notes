# Notes from 29 June, Assignment 2
## HTML
### Wireframing
- Wireframing allows developers to define and plan for the hierarchy of their design for a website or application.
- When designing knowing where your product puts your information should be done prior to building anything with code. 
- Wireframing is also a great way to know how a user will interact with your interface without the distractions of colors, font, or styling.
- When creating a wireframe, some developers like to draw them by hand while others feel more comfortable using some type of software like [Invision](https://www.google.com) or [Balsamiq](https://www.google.com).
- Here is an example of a hand-drawn wireframe.
![Hand-drawn Wireframe](https://careerfoundry.com/en/wp-content/uploads/old-blog-uploads/versions/xsamuel-student-wireframe---x----972-715x---.png.pagespeed.ic.eBpEWaqn7d.webp)

### Tools
- Some tools that are handy for helping create effective wireframing include:
1. UXPin: Useful facilitation of building responsive clickable prototypes directly in your browser.
2. InVision: Allows feedback to get straight from your team and users through clickable mock-ups of your site design. Free!
3. Wireframe.cc: Technology to create wireframes really quickly within your browser: the online version of pen and paper.

How to make your wireframe in six steps
1. Do your research
2. Prepare your research for quick reference
3. Make sure you have your user flow mapped out
4. Draft, don’t draw. Sketch, don’t illustrate
5. Add some detail and get testing
6. Start turning your wireframes into prototypes

## HTML Basics
- HTML (Hypertext Markup Language) is the code that is used to structure a web page and its content. HTML is a markup language that defines the structure of your content. 

### Anatomy of an HTML Element

- The main parts of our element are as follows:

1. The opening tag.
2. The closing tag.
3. The content.
4. The element.
 ### Elements can also have attributes
 - Attributes contain extra information about the element that you don't want to appear in the actual content. Here, class is the attribute name and editor-note is the attribute value. The class attribute allows you to give the element a non-unique identifier that can be used to target it (and any other elements with the same class value) with style information and other things.
 - An attribute should always have the following:
 - A space between it and the element name (or the previous attribute, if the element already has one or more attributes).
- The attribute name followed by an equal sign.
- The attribute value wrapped by opening and closing quotation marks.

### Anatomy of an HTML Document
`<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>`
`!DOCTYPE html` — doctype. It is a required preamble. In the mists of time, when HTML was young (around 1991/92), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML, which could mean automatic error checking and other useful things. However these days, they don't do much and are basically just needed to make sure your document behaves correctly. That's all you need to know for now.
`html` — the <html> element. This element wraps all the content on the entire page and is sometimes known as the root element.
`head` — the <head> element. This element acts as a container for all the stuff you want to include on the HTML page that isn't the content you are showing to your page's viewers. This includes things like keywords and a page description that you want to appear in search results, CSS to style our content, character set declarations, and more.
`meta charset="utf-8"` — This element sets the character set your document should use to UTF-8 which includes most characters from the vast majority of written languages. Essentially, it can now handle any textual content you might put on it. There is no reason not to set this and it can help avoid some problems later on.
`title` — the <title> element. This sets the title of your page, which is the title that appears in the browser tab the page is loaded in. It is also used to describe the page when you bookmark/favorite it.
`body` — the <body> element. This contains all the content that you want to show to web users when they visit your page, whether that's text, images, videos, games, playable audio tracks, or whatever else.

### Other Important Elements
- p - paragraph
- h1 - h6 = headings, same as markdown's "#" functionality.
- ul - unordered list
- ol - ordered list
- a - anchor tag
- href - allows to hyperlink images, websites, or other documents


## Semantics
- Semantics refers to the meaning of a piece of code or what effect it has on the functionality.

- These are some of the roughly 100 semantic elements available:

`<article>
<aside>
<details>
<figcaption>
<figure>
<footer>
<header>
<main>
<mark>
<nav>
<section>
<summary>
<time>`