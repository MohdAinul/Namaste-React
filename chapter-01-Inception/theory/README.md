# Chapter 01 - Inception

---

## Q: What is Emmet?

**A:**  
Emmet is the essential toolkit for web-developers. It allows you to type shortcuts that are then expanded into full pieces of code for writing HTML and CSS, based on an abbreviation structure most developers already use that expands into full-fledged HTML markup and CSS rules.

---

## Q: Difference between a Library and Framework?

**A:**  
A library is a collection of packages that perform specific operations whereas a framework contains the basic flow and architecture of an application.

The major difference between them is the complexity. Libraries contain a number of methods that a developer can just call whenever they write code.

React js is library and Angular is Framework.

The framework provides the flow of a software application and tells the developer what it needs and calls the code provided by the developer as required.

If a library is used, the application calls the code from the library.

---

## Q: What is CDN? Why do we use it?

**A:**  
A content delivery network (CDN) refers to a geographically distributed group of servers that work together to provide fast delivery of Internet content.

The main use of a CDN is to deliver content through a network of servers in a secure and efficient way.

---

## Q: Why is React known as React?

**A:**  
React is named React because of its ability to react to changes in data.

React is called React because it was designed to be a declarative, efficient, and flexible JavaScript library for building user interfaces.

The name React was chosen because the library was designed to allow developers to "react" to changes in state and data within an application, and to update the user interface in a declarative and efficient manner.

React is a JavaScript-based UI development library.

Facebook and an open-source developer community run it.

---

## Q: What is crossorigin in script tag?

**A:**  
The crossorigin attribute sets the mode of the request to an HTTP CORS Request.

The purpose of crossorigin attribute is used to share the resources from one domain to another domain.

Basically, it is used to handle the CORS request.

It checks whether it is safe to allow sharing the resources from other domains.

### Syntax

```html
<script crossorigin="anonymous|use-credentials"></script>
```

---

## Q: What is difference between React and ReactDOM?

**A:**  
React is a JavaScript library for building User Interfaces whereas ReactDOM is also JavaScript library that allows React to interact with the DOM.

The **react package** contains:

- React.createElement()
- React.Component
- React.Children

These helpers are used to build components.

The **react-dom package** contains:

- ReactDOM.render()

And in **react-dom/server** we have server-side rendering support with:

- ReactDOMServer.renderToString()
- ReactDOMServer.renderToStaticMarkup()

---

## Q: What is difference between react.development.js and react.production.js files via CDN?

**A:**  
Development is the stage of an application before it's made public while production is the term used for the same application when it's made public.

Development build is several times (maybe 3–5x) slower than the production build.

---

## Q: What is async and defer?

### Async

The async attribute is a boolean attribute.

The script is downloaded in parallel (in the background) to parsing the page, and executed as soon as it is available.

It does not block HTML DOM construction during downloading process and doesn’t wait for anything.

```html
<script src="demo_async.js" async></script>
```

---

### Defer

The defer attribute is a boolean attribute.

The script is downloaded in parallel (in the background) to parsing the page, and executed after the page has finished parsing (when browser finished DOM construction).

The defer attribute tells the browser not to wait for the script.

Instead, the browser will continue to process the HTML and build the DOM.

```html
<script src="demo_defer.js" defer></script>
```

---

## Using Module Scripts

Unless you're supporting ancient legacy systems, always add `type="module"` to all your script tags.

```html
<script type="module" src="main.js"></script>
```

Place the tag inside the `<head>`.

```html
<script defer nomodule></script>
```

can be used as a legacy fallback.

---

### Advantages of Module Scripts

- Allows you to import modules, which makes it easier to organize your code.
- Enables strict mode by default.
- Makes your code run faster and reports more runtime errors instead of silently ignoring them.
- Executes your code only after the DOM has initialized.
- Makes DOM manipulation easier.
- Prevents top-level variables from implicitly polluting the global namespace.
- Allows you to use top-level await in supported engines.
- Loads and parses your code asynchronously which improves load performance.