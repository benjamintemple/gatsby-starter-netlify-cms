---
templateKey: 'about-page'
path: /about
title: About our values
---
# Intro to React
A step-by-step guide for getting started with React.

React is one of the most powerful and popular ways to build user-interfaces for websites, web applications, and mobile devices.  In this tutorial, we'll see what React looks like, where you put your React code, and look at some of the special features in React that makes it so popular.

Generally speaking, most of the UI work you've done up until now has had to involve a lot of clunky code to make data requests, handle responses, render the data on the screen in a table, and update different parts of the website where you have to mix HTML and JavaScript.

## Step 1 - What does React Look Like?

React calls itself "a JavaScript library for building UIs", which sounds accurate to me!  But what's different about React than what you've already learned?

1. JSX
2. Components
3. Props
4. State

For now, just take a look at the code below.  Babel is a JavaScript compiler (which lets us write short hand, then converts it to JavaScript for output.  So the Babel tab is just JavaScript.  Also be sure to check out the HTML tab.

In the "HTML" tab, we have only 1 line, which is just an empty div with an id of root.  With React, we have to have a DIV that our compiled React code actually gets displayed.  The id can be anything you want, we're just using "root" here.

```HTML
<div id="root"></div>
```

In the Babel tab, we just have some simple code.  `ReactDom.render()` is a special React method that actually renders your content to the screen.  It takes 2 arguments: what to render, and where to render it.

```JavaScript
ReactDOM.render(
  <h1>Hello World</h1>,
  document.getElementById('root')
);
```

In the example above, the first argument, or "what to render", just contains plain HTML.  The second argument, or "where to render it too" is going to point to the HTML element where we want to show our output.  In this case, it's going to look for an HTML element with an id of root and render it there.

But wait a minute... what is the deal with sticking HTML inside of a JavaScript method/function?  Well... it's not EXACTLY HTML, but it's pretty darn close!  In React-speak, we call it JSX.  Fancy name, right?  But it's pretty simple stuff.  One of the main responsiblities of a UI is to mix HTML and JS together to display content on the screen.  JSX gives us an easy way to mix the 2 and get our results, and that easy way is called JSX.

## Web Components

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="rNWEwXP" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Web Components">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/rNWEwXP">
  Web Components</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## ReactDOM.render() and Rendering Elements

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="abBrQeo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React - Hello World">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/abBrQeo">
  React - Hello World</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Let's take a look at the example below.  This time, we've declared 2 variables.  We have 'name' which is equal to 'World!'... speaks for itself.  But then we have what appears to be HTML, sort of, with `const element = <h1>Hello {name}</h1>`.  What's that all about?  That's JSX, the special little shortcut lanauge we use with React that gets compiled automatically by Babel.

Let's break it down.  In JSX, you can insert any valid JavaScript you want inside of curley brackets.  It can be a variable name, a function, or any other valid JavaScript.  One thing you probably noticed is that there are no quotation marks around `<h1>Hello {name}</h1>` like you'd probably expect.  That's just JSX.

So in this example, we made a variable, name, set to World!", and another variable named element which consits of an `<h1>` tag with the worlds "Hello " followed by the value of the 'name' variable.  In plain JavaScript, we might write it like this:

```javascript
const name = "World";
const element = "Hello " + name;
document.getElementById("root").innerHTML = element;
```




First, we have our `ReactDOM.render` method which defines what to display and where to display it.



## JSX and ReactDOM.render()

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="abBrQeo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React - Hello World">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/abBrQeo">
  React - Hello World</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## JSX with Variables

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="bGBPBwP" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React - JSX">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/bGBPBwP">
  React - JSX</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Comments in JSX

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="KKNjaje" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React Comments">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/KKNjaje">
  React Comments</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## React Components

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="gOLJZZj" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React - Hello World Component">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/gOLJZZj">
  React - Hello World Component</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Multiple Components

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="rNWEjZQ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React - Hello World Multiple Components">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/rNWEjZQ">
  React - Hello World Multiple Components</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## React Props

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-user="bdtskc" data-slug-hash="KKNjaNv" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="React - Hello World Props">
  <span>See the Pen <a href="https://codepen.io/bdtskc/pen/KKNjaNv">
  React - Hello World Props</a> by BDTSKC (<a href="https://codepen.io/bdtskc">@bdtskc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
