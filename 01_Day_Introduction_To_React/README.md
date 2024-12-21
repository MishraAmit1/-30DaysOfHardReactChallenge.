<div align="center">
  <h1> 30 Days Of React: Getting Started React</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/amsmishra/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://x.com/ezYams">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/ezYams?style=social">
  </a>

<sub>Author:
<a href="https://www.linkedin.com/in/amsmishra/" target="_blank">Amit Mishra</a><br>
<small> December 20, 2024</small>
</sub>

</div>

[<< Day 1](../01_Day_Introduction_To_React/README.md) | [Day 3 >>](../03_Day_Setting_Up/README.md)

![30 Days of Hard React banner](./images/banner.webp)

## Table of Contents

- [1. What is React?](#1-what-is-react)
- [2. JSX](#2-jsx)

  - [2.1 JSX Element](#21-jsx-element)
  - [2.2 Commenting a JSX Element](#32-commenting-a-jsx-element)
  - [2.3 Rendering a JSX Element](#33-rendering-a-jsx-element)
  - [2.4 Style and className in JSX](#34-style-and-classname-in-jsx)
  - [2.5 Injecting Data to a JSX Element](#35-injecting-data-to-a-jsx-element)
    - [2.5.1 Injecting a String to a JSX Element](#351-injecting-a-string-to-a-jsx-element)
    - [2.5.2 Injecting a Number to a JSX Element](#352-injecting-a-number-to-a-jsx-element)
    - [2.5.3 Injecting an Array to a JSX Element](#353-injecting-an-array-to-a-jsx-element)
    - [2.5.4 Injecting an Object to a JSX Element](#354-injecting-an-object-to-a-jsx-element)

- [4. Exercises](#4-exercises)
  - [4.1 Exercises: What is React?](#41-exercises-what-is-react)
  - [4.2 Exercises: Why React?](#42-exercises-why-react)
  - [4.3 Exercises: JSX](#43-exercises-jsx)
  - [4.4 Exercises: JSX Elements](#44-exercises-jsx-elements)
  - [4.5 Exercises: Inline Style](#45-exercises-inline-style)
  - [4.6 Exercises: Internal Styles](#46-exercises-internal-styles)
  - [4.7 Exercise: Inject Data to JSX](#47-exercise-inject-data-to-jsx)

---

### 1. What is React?

# React: A Powerful JavaScript Library

React is a **JavaScript library** created by **Facebook (now Meta)** for building **user interfaces (UI)**, especially for **web applications**. It's used to create fast, interactive, and dynamic websites.

---

## 🌟 Why Use React?

- **Speed**: React updates the page quickly without reloading it.
- **Reusability**: Build components once and reuse them across your app.
- **Community**: A large ecosystem with lots of tools, libraries, and resources.

---

## 📚 Key Concepts

<details>
<summary>🔹 Component-Based</summary>
React breaks the UI into small, reusable pieces called **components** (like LEGO blocks). Each component manages its own logic and UI, making your app modular and easy to maintain.
</details>

<details>
<summary>🔹 Virtual DOM</summary>
React uses a **Virtual DOM**, which is a lightweight copy of the real DOM. This makes updates faster because React only changes what’s necessary instead of re-rendering the whole page.
</details>

<details>
<summary>🔹 Declarative</summary>
With React, you describe **what you want** your UI to look like, and React handles **how to achieve it**. This approach makes your code cleaner and easier to debug.
</details>

<details>
<summary>🔹 Single-Page Applications (SPAs)</summary>
React is great for creating **SPAs**, where only parts of the page update dynamically without reloading the entire page. This results in a smoother, faster user experience.
</details>

---

## 💡 Example to Understand React

Imagine you're building a **social media app** like Facebook:

- React helps you create buttons, posts, and feeds.
- These elements update dynamically without refreshing the whole page.

---

# What is SPA (Single-Page Application)?

SPA stands for **Single-Page Application**. It’s a type of web application that loads **one single HTML page** and dynamically updates the content on the page **without reloading the entire page**. This results in a smoother and faster user experience.

React is perfect for building SPAs.

---

## 🔍 Normal Website vs SPA

<details>
<summary>🔸 **Normal Website (Multi-Page Application)**</summary>
- Every time a user visits a new page, the entire page reloads from the server.  
- **Example**: On a blog, moving from "Home" to "About Us" reloads the whole page.
</details>

<details>
<summary>🔸 **SPA (Single-Page Application)**</summary>
- The first page (HTML, CSS, JS) is loaded only once.  
- After that, data is fetched and updated dynamically, without reloading the entire page.  
- **Example**: Gmail. When you open a new email, only the email content changes while the rest of the page (header, sidebar) remains unchanged.
</details>

---

## ⚙️ How Does SPA Work?

<details>
<summary>Step-by-Step Explanation</summary>

1. **First Load**:  
   The server sends a single HTML file along with JavaScript.

2. **After That**:
   - JavaScript (React, for instance) dynamically updates only the parts of the page that need to change.
   - The **Virtual DOM** helps React figure out what has changed and updates only that part without touching the rest of the page.
   </details>

---

## 📖 Real-Life Examples of SPA

<details>
<summary>Examples You Can Relate To</summary>

1. **Facebook Feed**:

   - When you click the "Like" button, only that post gets updated.
   - The rest of the page stays the same.

2. **Gmail**:

   - Switching between emails updates the content dynamically without reloading the entire app.

3. **Instagram/Twitter**:
   - Scrolling through the feed or interacting with posts works seamlessly as an SPA.

</details>

---

## 🔗 Explore More

For more details on React, visit the [official documentation](https://reactjs.org/).

### 2. What is JSX?

JSX stands for JavaScript XML. It's a syntax extension for JavaScript that looks similar to HTML, but it's used within JavaScript to describe what the UI should look like. JSX allows us to write HTML elements in JavaScript and place them in the DOM.

## Why Use JSX?

- **Declarative Syntax**: JSX allows developers to write HTML-like structures directly in JavaScript. It is much easier to understand and maintain.
- **JavaScript Expression Support**: JSX allows embedding JavaScript expressions inside curly braces `{}`.

### Example:

```jsx
const element = <h1>Hello, world!</h1>;
```

## ➕ Important Points:

- **JSX** is not a requirement for React, but it's widely used because it makes code easier to read and write.
- **React** uses a tool called Babel to convert JSX into regular JavaScript.

#### Commenting a JSX element

We comment codes for different reasons and it is also good to know how to comment out JSX elements in React.

```js
{
  /*
 <header>
    <h1>Welcome to 30 Days Of React</h1>
    <h2>Getting Started React</h2>
    <h3>JavaScript Library</h3>
    <p>Asabeneh Yetayeh</p>
    <small>Oct 2, 2020</small>
  </header>

*/
}
```

## Rendering JSX to the DOM

To render JSX to the DOM, we use ReactDOM.render() method. This method takes two arguments:

1. The JSX or React component you want to render.
2. The DOM element where you want to render the content.

Example:

```jsx
import React from "react";
import ReactDOM from "react-dom";

const element = <h1>Hello, world!</h1>;

ReactDOM.render(element, document.getElementById("root"));
```

In this example, (the Hello, world!) JSX is rendered inside the DOM element with the id="root".

#### 2.3 Rendering a JSX Element

To render JSX into the DOM, React uses the ReactDOM.render() method.

Example:

```jsx
import React from "react";
import ReactDOM from "react-dom";

const element = <h1>Hello, world!</h1>;

ReactDOM.render(element, document.getElementById("root"));
```

This will render <h1>Hello, world!</h1> inside the DOM element with id="root".

#### 2.4 Style and className in JSX

In JSX, we can add inline styles to elements using the `style` attribute. The `style` attribute in JSX is an object where keys are camelCased CSS properties and values are strings representing the corresponding CSS values.

##### Example 1: Inline Style

```js
const header = (
  <header
    style={{ border: "2px solid orange", color: "black", fontSize: "18px" }}
  >
    <h1>Welcome to 30 Days Of React</h1>
    <h2>Getting Started React</h2>
    <h3>JavaScript Library</h3>
    <p>Asabeneh Yetayeh</p>
    <small>Oct 2, 2020</small>
  </header>
);
```

##### Example 2: Using a Style Object

You can also define the styles outside the JSX element using a JavaScript object and then apply it:

```js
const style = { border: "2px solid orange", color: "black", fontSize: "18px" };

const header = (
  <header style={style}>
    <h1>Welcome to 30 Days Of React</h1>
    <h2>Getting Started React</h2>
    <h3>JavaScript Library</h3>
    <p>Asabeneh Yetayeh</p>
    <small>Oct 2, 2020</small>
  </header>
);
```

##### Example 3: Using className for CSS Classes

To apply traditional CSS styles (i.e., external or internal styles), we use className in JSX, similar to how we use class in HTML. This allows us to assign CSS classes to elements.

```js
const element = (
  <div style={{ color: "blue", fontSize: "20px" }} className="my-class">
    Hello, styled world!
  </div>
);
```

In this example, the element will have inline styling (blue color and font size of 20px) along with the class my-class. You can define the class in an external CSS file:

```css
.my-class {
  font-weight: bold;
  text-align: center;
}
```

This approach combines inline styles with external CSS for better styling management.
