# [JavaScript Mentoring Program](../README.md)

## 3 JavaScript Basics

The first what you should understand that NO ONE really know JavaScript, just deal with it. All we are humans, I hope, and humans are doing mistakes, probably this is why you are here and trying learning JavaScript with me. We are going just to start learning, so do not try remember all and read all what I will share with you today. This is just the course materials.

> So let's get started!

## 3.1 What is JavaScript?

JavaScript is a text-based programming language used both on the client-side and server-side that allows you to make web pages interactive. Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user. Common examples of JavaScript that you might use every day include the search box on Amazon, a news recap video embedded on The New York Times, or refreshing your Twitter feed.  

Incorporating JavaScript improves the user experience of the web page by converting it from a static page into an interactive one. To recap, JavaScript adds behavior to web pages.

## 3.2 What is JavaScript used for?

JavaScript is mainly used for web-based applications and web browsers. But JavaScript is also used beyond the Web in software, servers and embedded hardware controls. Here are some basic things JavaScript is used for:

### 1. Adding interactive behavior to web pages

JavaScript allows users to interact with web pages. There are almost no limits to the things you can do with JavaScript on a web page – these are just a few examples:

- Show or hide more information with the click of a button
- Change the color of a button when the mouse hovers over it
- Slide through a carousel of images on the homepage
- Zooming in or zooming out on an image
- Displaying a timer or count-down on a website
- Playing audio and video in a web page
- Displaying animations
- Using a drop-down hamburger menu

### 2. Creating web and mobile apps

Developers can use various JavaScript frameworks for developing and building web and mobile apps. JavaScript frameworks are collections of JavaScript code libraries that provide developers with pre-written code to use for routine programming features and tasks—literally a framework to build websites or web applications around.

Popular JavaScript front-end frameworks include React, React Native, Angular, and Vue. Many companies use Node.js, a JavaScript runtime environment built on Google Chrome’s JavaScript V8 engine. A few famous examples include Paypal, LinkedIn, Netflix, and Uber!

### 3. Building web servers and developing server applications

Beyond websites and apps, developers can also use JavaScript to build simple web servers and develop the back-end infrastructure using Node.js.

### 4. Game development

Of course, you can also use JavaScript to create browser games. These are a great way for beginning developers to practice their JavaScript skills.

## 3.3 How JavaScript work?

### 1. The JavaScript Engine

The way JavaScript works is interesting. Inside a normal Web page you place some JavaScript code (See How Web Pages Work for details on Web pages). When the browser loads the page, the browser has a built-in interpreter that reads the JavaScript code it finds in the page and runs it.

JavaScript executed by JavaScript Engine. A popular example of a JavaScript Engine is Google’s V8 engine. The V8 engine is used inside Chrome and Node.js for example. Here is a very simplified view of what it looks like:

![o](./assets/1.png "JS Memory Usage")

The Engine consists of two main components:

- Memory Heap — this is where the memory allocation happens
- Call Stack — this is where your stack frames are as your code executes

### 2. The Runtime

There are APIs in the browser that have been used by almost any JavaScript developer out there (e.g. “setTimeout”). Those APIs, however, are not provided by the Engine.
So, where are they coming from?
It turns out that the reality is a bit more complicated.

![o](./assets/2.png "JS Memory Usage")

More about that you can read here [How does javascript actually work](https://blog.sessionstack.com/how-does-javascript-actually-work-part-1-b0bacc073cf)

## 3.4 Home Task

Read about JavaScript History, and basic logical operators. From any source you like. I also added recommended links below.

### HTML file structure

Create an HTML file on your desktop. With structure like this.
Or just follow the link to open online javascript executor.
[Just Try It >](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_default_default)

```HTML
<!DOCTYPE html>
<html>
<head>
</head>
<body>
<h2>JavaScript Mentoring Program - JavaScript Basics</h2>
</body>
</html>
```

Add into `body` section a few tags:

```HTML
<p id="home-task">Here we have some text!</p>
<button type="button" onclick="myFunction()">Try it</button>
```

### The Script Tag

The `<script>` tag is what we use to includes our JavaScript. It's a lot like the `<link>` tag you've already been using to include your CSS files.

Here's a very basic snippet of JavaScript using the script tag. This JavaScript is written directly into our HTML page. It will call and alert box as soon as the page loads.

```HTML
<script type="text/javascript">
  alert("This alert box was called with the onload event");
</script>
```

You will see this alert message on a page.

### A Function Creation and execution

The try to implement your oun function which will be called when you press the button.

```javascript
function myFunction() {
  document.getElementById("home-task").innerHTML = "Your oun text";
}
```

### Final Task

Change function in the way that each time when you click on the button it should show in the `home-task` paragraph current date and time in format `DD-MM-YYYY HH:MM:SS`

## Materials to saved to the bookmarks

- [History of JavaScript](https://en.wikipedia.org/wiki/JavaScript)
- [JavaScript.info](https://javascript.info/)
- [JavaScript Tutorial for Beginners: Learn JavaScript in 1 Hour](https://www.youtube.com/watch?v=W6NZfCO5SIk&ab_channel=ProgrammingwithMosh)
- [JavaScript Main site](https://www.javascript.com/)
- [JavaScript - MDN Web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript Handbook](http://edu-9.de/uploads/books/javascript-handbook.pdf)
- [10 Most Common mistakes](https://www.toptal.com/javascript/10-most-common-javascript-mistakes)
