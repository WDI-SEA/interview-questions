## HTML Questions

* What does a `doctype` do?

The doctype is an instruction to the web browser to let it know which mark up language is being used. It refers to it's document type identification.

* What's the difference between HTML and XHTML?
HTML and XHTML are both from XML. The main differences are that XHTML must be properly nested, closed, lowercase, and have one root element.

* What are `data-` attributes good for?

Data attributes allow you to assign custom data to an element. 

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
Cookie: A message given from the web browser to the web server. The cookie is used to identify users, and will save info about this user on the web server for a later date when the user visits the site again.

sessionStorage: When a user is on the webpage their data is being stored in a session. This session gets cleared when a session ends. A session ends when the browser is closed.

localStorage: Hard drive or solid state of the device being referenced.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

The program reads from top to bottom so you want the program to read your css before it starts rendering anything in the body. The same can be said for the script tags, however, if you put your script tags at the bottom of the page that could block your browser from accessing your script tags.
