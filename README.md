# Introduction
In this part, we will familiarize ourselves with the practicalities of taking the course. After that, we will have an overview of the basics of web development and also talk about the advances in web application development during the last few decades.
***
## General Info
This course is an introduction to modern web development with JavaScript. The main focus is on single-page applications implemented with React and supporting them with RESTful and GraphQL web services implemented with Node.js. The course also has parts on TypeScript, React Native, and Continuous integration.

Other topics include debugging applications, container technology, configuration, managing runtime environments, and databases.

### Prerequisites
Participants are expected to have good programming skills, basic knowledge of web programming and databases, and know the basics of the Git version control system. You are also expected to have perseverance and a capacity for solving problems and seeking information independently.

`Previous knowledge of JavaScript or other course topics is not required.`

How much programming experience is needed? It is hard to say, but you should be pretty fluent with your language. This level of fluency takes usually at least 100-200 hours of practice to develop.

### Before you start
Using the Chrome browser is recommended for this course because it provides the best tools for web development. Another alternative is the Developer Edition of Firefox, which provides the same range of features.

The course exercises are submitted to GitHub, so Git must be installed and you should know how to use it. For instructions, see Git and GitHub tutorial for beginners.
Install a sensible text editor that supports web development. Visual Studio Code is highly recommended.

Don't code with nano, Notepad or Gedit. NetBeans isn't very good for web development either. It is also rather heavy in comparison to Visual Studio Code.

Also, install Node.js. The material has been done with version 18.13.0, so don't install any version older than that. See Node.js installation instructions.

Node package manager npm will be automatically installed with Node.js. We will be actively using npm throughout the course. Node also comes with npx, which we'll need a few times.
***
## Fundamental of Web apps
**The 1st rule of web development**: `Always keep the Developer Console open` on your web browser. On macOS, open the console by pressing fn-F12 or option-cmd-i simultaneously. On Windows or Linux, open the console by pressing Fn-F12 or ctrl-shift-i simultaneously.

`The most important tab is the Console tab.`

The server and the web browser communicate with each other using the HTTP protocol. The Network tab shows how the browser and the server communicate

#### Traditional web applications
 When entering the page, the browser fetches the HTML document detailing the structure and the textual content of the page from the server. In traditional web applications, the browser is "dumb". It only fetches HTML data from the server, and all application logic is on the server.
 
 #### Event Handlers & Callback Functions
 The mechanism of invoking event handlers is very common in JavaScript. Event handler functions are called callback functions. The application code does not invoke the functions itself, but the runtime environment - the browser, invokes the function at an appropriate time when the event has occurred.
```
xhttp.onreadystatechange = function() {
  if (this.readyState == 4 && this.status == 200) {
    // code that takes care of the server response
  }
}
```

#### Document Object Model | Dom
We can think of HTML pages as implicit tree structures. The same treelike structure can be seen on the console tab Elements.

The functioning of the browser is based on the idea of depicting HTML elements as a tree.
Document Object Model, or DOM, is an Application Programming Interface (API) that enables programmatic modification of the element trees corresponding to web pages.

### AJAX
[AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) (Asynchronous JavaScript and XML) is a term introduced in February 2005 on the back of advancements in browser technology to describe a new revolutionary approach that enabled the fetching of content to web pages using JavaScript included within the HTML, without the need to rerender the page.

Before the AJAX era, all web pages worked like the traditional web application.

### Single page app
In recent years, the Single-page application (SPA) style of creating web applications has emerged. SPA-style websites don't fetch all of their pages separately from the server, but instead comprise only one HTML page fetched from the server, the contents of which are manipulated with JavaScript that executes in the browser.

### Javascript Libraries
* * *
#### JQuery
jQuery was developed back when web applications mainly followed the traditional style of the server generating HTML pages, the functionality of which was enhanced on the browser side using JavaScript written with jQuery. One of the reasons for the success of jQuery was its so-called cross-browser compatibility. The library worked regardless of the browser or the company that made it, so there was no need for browser-specific solutions. Nowadays using jQuery is not as justified given the advancement of JavaScript, and the most popular browsers generally support basic functionalities well.

#### Furthur mentions
The rise of the single-page app brought several more "modern" ways of web development than jQuery. The favorite of the first wave of developers was BackboneJS. After its launch in 2012, Google's AngularJS quickly became almost the de facto standard of modern web development.

However, the popularity of Angular plummeted in October 2014 after the Angular team announced that support for version 1 will end, and that Angular 2 will not be backwards compatible with the first version. Angular 2 and the newer versions have not gotten too warm of a welcome.

Currently, the most popular tool for implementing the browser-side logic of web applications is Facebook's React library. During this course, we will get familiar with React and the Redux library, which are frequently used together.

The status of React seems strong, but the world of JavaScript is ever-changing. For example, recently a newcomer - VueJS - has been capturing some interest.

### Full-stack web development
***
What does Full-stack web development mean?. There is no agreed-upon definition for the term.
Practically all web applications have (at least) two "layers": the browser, being closer to the end-user, is the top layer, and the server the bottom one. There is often also a database layer below the server. We can therefore think of the architecture of a web application as a stack of layers.

Often, we also talk about the frontend and the backend. The browser is the frontend, and the JavaScript that runs on the browser is the frontend code. The server on the other hand is the backend.
Using the same programming language on multiple layers of the stack gives full-stack web development a whole new dimension. However, it's not a requirement of full-stack web development to use the same programming language (JavaScript) for all layers of the stack.

It used to be more common for developers to specialize in one layer of the stack, for example, the backend. Technologies on the backend and the frontend were quite different. With the Full stack trend, it has become common for developers to be proficient in all layers of the application and the database. Oftentimes, full-stack developers must also have enough configuration and administration skills to operate their applications, for example, in the cloud.

