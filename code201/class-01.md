# Code 201 - Reading Notes
## Introduction to HTML and Javascript
### HTML
#### What is it and how does it work?
- HTML means Hypertext Markup Language.
- It is the code that is used to set up the structure of a web page and its general content.
#### Anatomy of an HTML Document
- `!DOCTYPE html` — The document type. This is required to make sure the document behaves correctly.
- `html` — Encompasses all content in the code aside from the doctype.
- `head` — Acts as a container for all the coding and styling not included in the content you intend to show on the webpage. This means things like language, character sets, keywords, and a description that appears when you Google your website. Other universal settings and elements are included here as well.
- `meta charset="utf-8"` — Picks the character set your document should use to UTF-8. This includes most characters from the majority of written languages.
- `title` — Title of the page. The title that appears in the browser tab the page is loaded in and when bookmarked.
- `header` - Where the navigation and main caption of the webpage is.
- `body` — All the content that you want to show to your website viewers.
- `footer` - bottom of the page, contains copyright, links, contact, other useful links.

#### Extra Markup 
<!-- Used book "HTML and CSS" by Jon Duckett pgs. 177 - 191 for these definitions -->
- Doctype - tells the browser what type of file you're using.
- Comment - contain helpful information about your website.
- id attribute - uniquely identifies an element.
- class attribute - can be used to uniquely identify multiple elements of simliar use/composition.
- div element - group a set of elements together in one block-level box.
- span element - an inline div element. Use to contain a section of text where there is no other suitable element to differentiate from its surrounding text. Most commonly used to control the appearance of content using CSS.
- iframe element - little window inside your webpage that displays another webpage. Most commonly used for GoogleMaps. Can control things like height, width, scrolling, frameborder, and seamless attirbutes of the iframe element.

### Javascript
#### What is Javascript?
- Javascript is a just-in-time compiled programming language.
- Well known for as the scripting language for websites and non-browser environments (like Node.js Apache CouchDB, and Adobe Acrobat).
- JavaScript is a programming language that allows you to implement complex features on web pages such as displaying timely content updates, interactive maps, animated 2D/3D graphics, scrolling video jukeboxes.
- Javascript and Java are different in syntax, semantic, and use.
<!-- obtained the information below this comment from "Javascript and JQuery" by Jon Duckett -->
- Javascript usese scripts to function.
- A script is a series of instructions like a recipe, handbook, or manual.

#### Programming Noteables
- Objects - a physical thing in the real world
- Properties - characterisitcs that make up objects, like color, size, spacing.
- Event - ways that users interact with objects. computer's way of saying "hey, this just happened!"
- Methods - represent how people or other things interact with the object in the real world. Can tell you something about an object or change an objects value.
- Example would be `document.write('Hello World!");`, where `document` would be the object and `write('Hello World!)` would be the method. The `.` is the allows access to the object's members and methods.

[BACK TO HOME](reading-notes/README.md)