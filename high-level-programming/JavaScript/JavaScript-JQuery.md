# JavaScript - Web jQuery

## What is JavaScript

- JavaScript is a scripting or programming language that allows you to implement complex features on web pages
  - HTML is the markup language that we use to structure and give meaning to our web content
  - CSS is a language of style rules that we use to apply styling to our HTML content
  - JavaScript is a scripting language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else
- A very common use of JavaScript is to dynamically modify HTML and CSS to update a user interface, via the Document Object Model API

### JavaScript running order
- When the browser encounters a block of JavaScript, it generally runs it in order, from top to bottom

### Interpreted versus compiled code

- In interpreted languages, the code is run from top to bottom and the result of running the code is immediately returned
- Compiled languages on the other hand are transformed (compiled) into another form before they are run by the computer
- JavaScript is a lightweight interpreted programming language. The web browser receives the JavaScript code in its original text form and runs the script from that

### Server-side versus client-side code

- Client-side code is code that is run on the user's computer
- In this module we are explicitly talking about client-side JavaScript.
- Server-side code on the other hand is run on the server, then its results are downloaded and displayed in the browser
- JavaScript can also be used as a server-side language, for example in the popular Node.js environment

### Dynamic versus static code

- The word dynamic is used to describe both client-side JavaScript, and server-side languages
- JavaScript dynamically generates new content inside the browser on the client, e.g. creating a new HTML table
- A web page with no dynamically updating content is referred to as static — it just shows the same content all the time.

### How do you add JavaScript to your page?

- JavaScript is applied to your HTML page in a similar manner to CSS.
- JavaScript only needs one friend in the world of HTML — the `<script>` element
- **External JavaScript**
  - First, create a new file in the same directory as your sample HTML file, say `script.js`
  - Replace your current <script> element with `<script src="script.js" defer></script>`
  - Inside `script.js` write your code
- **Inline JavaScript handlers**
  - Note that sometimes you'll come across bits of actual JavaScript code living inside HTML
  - Please don't do this, however. It is bad practice to pollute your HTML with JavaScript, and it is inefficient

### Script loading strategies

- There are a number of issues involved with getting scripts to load at the right time.
- A common problem is that all the HTML on a page is loaded in the order in which it appears
- If you are using JavaScript to manipulate elements on the page (or more accurately, the Document Object Model), your code won't work if the JavaScript is loaded and parsed before the HTML you are trying to do something to
- we use a more modern JavaScript feature to solve the problem, the `defer` attribute, which tells the browser to continue downloading the HTML content once the `<script>` tag element has been reached, as in: `<script src="script.js" defer></script>`

### async and defer

- There are actually two modern features we can use to bypass the problem of the blocking script — `async` and `defer`
- Scripts loaded using the `async` attribute will download the script without blocking the page while the script is being fetched. However, once the download is complete, the script will execute, which blocks the page from rendering.
-  It is best to use `async` when the scripts in the page run independently from each other and depend on no other script on the page.
- Scripts loaded with the `defer` attribute will load in the order they appear on the page. They won't run until the page content has all loaded, which is useful if your scripts depend on the DOM being in place