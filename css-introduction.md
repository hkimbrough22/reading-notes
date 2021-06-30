# Notes from 30 June
## CSS Introduction
### What is CSS?
- CSS stands for Cascading Style Sheets. 
- It is the language for specifying how your documents are presented on your website.
- This includes basic colors, animations, size of certain features.
- CSS is a rule-based language meaning that you must define the rules pertaining to specific groups of code that you want the CSS applied to.
- The rule syntax opens with a selector. This picks the element that you want to currently style. This can be `p` or `h1` or even `body`.
- We then have a set of curly braces `{ }`. Inside the brackets you will have one or more declarations.
- Declarations syntax always has a property and a value. The declaration specifies the property of the element(s) you want to style and then a value to give the property. Like this:
-`h1 {color: red;}`
- Here, before the colon, the property is "color" and after the colon is the value, "red". 
- A CSS stylesheet will have many rules.


### Other considerations
- CSS Modules - As there are so many things that you could style using CSS, the language is broken down into modules.
- CSS Specification - All web standards technologies (HTML, CSS, JavaScript, etc.) are defined in giant documents called specifications (or "specs"), which are published by standards organizations (such as the W3C, WHATWG, ECMA, or Khronos) and define precisely how those technologies are supposed to behave. CSS is no different — it is developed by a group within the W3C called the CSS Working Group.
- Browser support information - Once CSS has been specified then it is only useful for us in developing web pages if one or more browsers have implemented it. This means that the code has been written to turn the instruction in our CSS file into something that can be output to the screen.

### Inserting CSS
- When a website browser reads a certain style sheet, it will format the HTML document accordingly.
- There are three ways of inserting a style sheet:

- External CSS
- Internal CSS
- Inline CSS

#### External CSS
- An External CSS is an external style sheet that is linked to the HTML file in the `head` section.
- With an external style sheet, you can change the style of your entire site through changing one file.
- The external style sheet must be saved with a .css extension.

#### Internal CSS
-An internal style sheet is inside the `<style>` element, inside the `head` section.
- This is likely used if one single HTML page has a unique style.

#### Inline CSS
- Inline CSS is within a specific line of code pertinent to what you want styled.
- This is often used to apply a unique style for a single element.

#### Cascading Order
- This refers to the rules about which style would be used if there is more than one specific for an HTML element.
- The rules states these priority levels:
1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default
- This means that an inline style will override an external or internal styling.
