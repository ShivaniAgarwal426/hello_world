<div align="center"><h1> Explain everything related to Svelte  </h1></div>

## About SVELTE?
<img src="https://user-images.githubusercontent.com/70523057/136572595-f97910e5-3cbc-473a-937f-aaf948cb3d29.png" width="300" align = "right">

Svelte is a radical new approach to building user interfaces. Whereas traditional frameworks like React and Vue do the bulk of their work in the browser, Svelte shifts that work into a compile step that happens when you build your app.

Instead of using techniques like virtual DOM diffing, Svelte writes code that surgically updates the DOM when the state of your app changes.

Svelte was recently voted the  with the [most loved **web framework**](https://insights.stackoverflow.com/survey/2021#section-most-loved-dreaded-and-wanted-web-frameworks) in [most **experienced developers**](https://2020.stateofjs.com/en-US/technologies/front-end-frameworks/) a pair of industry surveys.



<div><a href="https://svelte.dev/tutorial"><em><strong>Learn more...</strong></em></a></div>

<br><br>

## What is SVELTE?
- Svelte is a free and open-source front end tool for building **fast web applications**.
- It is similar to JavaScript frameworks such as React and Vue, which share a goal of making it easy to build slick interactive user interfaces.
- But **there's a crucial difference:** 
  1. Svelte converts your app into ideal JavaScript at build time, rather than interpreting the application code at run time. 
  2. This is the reason we _don't pay the performance cost_ of the framework's abstractions, and we _don't incur a penalty_ when the app first loads.
- You can build your entire app with Svelte, or you can add it incrementally to an existing codebase. 
- You can also ship components as standalone packages that work anywhere, without the overhead of a dependency on a conventional framework.
- In Svelte, an application is composed from one or more components. <br> A component is a reusable self-contained block of code that encapsulates **`HTML`**, **`CSS`** and **`JavaScript`** that belong together, written into a `.svelte` file.

<br><br>

## How its works?
Most front-end frameworks rely on a diffing engine that syncs the visual DOM with an in-memory copy of the DOM.

**Svelte is different. It's a compiler.** It generates code (JavaScript) that updates the visual tree directly, without diffing.

_Think of it as converting html like `<h1>Hello World</h1>` into:_

```bash
const element = document.createElement('h1')
element.textContent = "Hello World"
document.body.appendChild(element)
```
> Now, why would you want to do that?
> **Because of data binding.**

It means we can write `<h1>{someValue}</h1>` declaratively and and we don't need to write imperative statements like `element.textContent = someValue` every time someValue changes.     <br>
Svelte generates the synchronization code for us.     <br>

The compiler takes in `.svelte` files, parses them into an **AST Abstract Syntax Tree**, **analyzes the tree**, and **generates Javascript and CSS**.

**You can try the Online Svelte Compiler**
<div align="center"><a href="https://svelte.dev/tutorial/"><table><tr><td><img src="https://user-images.githubusercontent.com/70523057/136598955-6fff83f0-cded-43a0-a752-88d038cd291b.png" width="800"><td><tr><table></a></div>
  
<div align="left">    <br>
  
## USES
  Let us see what are the advantages Svelte offers:
  - Compiler
  - Lightweight & Performant
  - Less boilerplate
  - Truly reactive
  - Low learning knowledge required
  - Built-in animations and effects
  - Built-in Reactive store
  - Multiple output targets (Svelte supports server-side rendering out of the box by providing a compiler mode for it.)
  
  <br><br>
  
## Summary
- Svelte is a compiler that parses `.svelte` files, analyzes them and then generates a JavaScript file. 
- The JavaScript file contains the logic to mount the component, handle events, and patch the DOM when values change.

</div>
