# Code 201 - Reading Notes
<!-- All notes were taken from Reading assignment 13 references in Jon Duckett's book and online references -->
## Local Storage
- Cookies created early in web's history - good for persistent local storage of small amounts of data. 
- But they have three potentially dealbreaking downsides:
  - Cookies are included with every HTTP request (slows down web app)
  - Cookies send data unencrypted over the internet, more or less.
  - Cookies are limited to roughly 4KB in size (enough to slow down system, but not enough to be useful).

- Goals for persistent local storage is a lot of storage space on the client, that persists beyond a page refresh, and isn’t transmitted to the server.

## HTML5 Storage
- A way webpages store key/value pairs locally within the browser. They are never transmitted to the server.
- User `localStorage` object on the global `window` object to access.
- HTML5 Storage is based on named key/value pairs. The named key is a string. The data can be any type including strings, Booleans, integers, or floats. However, the data is actually stored as a string.
- If you are storing and retrieving anything other than strings, you will need to use functions like `parseInt()` or `parseFloat()` to coerce your retrieved data into the expected JavaScript datatype.
- Calling `setItem()` with a named key that already exists will silently overwrite the previous value. Calling `getItem()` with a non-existent key will return null rather than throw an exception.
- 




[BACK TO HOME](../README.md)