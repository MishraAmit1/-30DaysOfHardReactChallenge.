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
<small> December 23, 2024</small>
</sub>

</div>

[<< Day 1](../01_Day_Introduction_To_React/README.md) | [Day 3 >>](../03_Day_Setting_Up/README.md)

![30 Days of Hard React banner](../01_Day_Introduction_To_React/images/banner.webp)

- [Setting Up](#setting-up)
  - [Node](#node)
  - [Module](#module)
  - [Package](#package)
  - [Node Package Manager(NPM)](#node-package-managernpm)
  - [Visual Studio Code](#visual-studio-code)
  - [Browser](#browser)
  - [Visual Studio Extensions](#visual-studio-extensions)
  - [Create React App](#create-react-app)
- [Your first React App](#your-first-react-app)
  - [React Boilerplate](#react-boilerplate)
  - [Styles in JSX](#styles-in-jsx)
  - [Injecting data to JSX elements](#injecting-data-to-jsx-elements)
  - [Importing Media Objects in React](#importing-media-objects-in-react)
- [Exercises](#exercises)
  - [Exercises: Level 1](#exercises-level-1)
  - [Exercises: Level 2](#exercises-level-2)
  - [Exercises: Level 3](#exercises-level-3)

# Day 3: Setting Up React

## 1. Node

### Explanation

Node.js is a runtime environment that allows JavaScript to run on the server side. Without Node.js, developing React applications isn’t possible because React requires a local development server, which Node.js provides.

### Real-life Example

Imagine you own a bakery. Node.js is like the oven that bakes the bread, and JavaScript is the dough. Without the oven (Node.js), the dough (JavaScript) cannot turn into bread. Similarly, React applications need Node.js to function.

---

### Commands to Install Node

1. Visit the [Node.js Official Site](https://nodejs.org/).
2. Download the **LTS version** (Long Term Support) for stability.
3. Install it on your system.
4. After installation, verify by running the following command in the terminal:

```bash
node -v
```

This will display the installed Node.js version.

---

### What is Node.js?

Node.js is an open-source, cross-platform JavaScript runtime environment used to execute JavaScript code on the server side. It is built on Chrome’s V8 JavaScript engine.

---

### Why Do We Use Node.js in React Projects?

1. **Package Management:**  
   React applications require various dependencies (libraries/modules) to function. Node.js provides npm (Node Package Manager), which is essential for managing these dependencies.

2. **Development Server:**  
   Node.js is required to run the development server provided by tools like Create React App.

3. **Speed and Scalability:**  
   Node.js uses an asynchronous and non-blocking architecture, making it highly efficient for performance-critical applications.

---

### Real-life Example

Think of a courier service that uses package management software to handle deliveries. Node.js is like that software, helping manage all React dependencies and running the project.

---

### Interview Questions

1. **What is Node.js, and why is it important for React development?**  
   Node.js is a runtime environment that allows JavaScript to be executed on the server side. It is crucial for React development because React relies on npm (part of Node.js) to manage libraries and tools.

2. **What is npm, and how is it used in React?**  
   npm (Node Package Manager) is a tool used to install and manage libraries (dependencies) in React applications, such as "react-router" or "redux."

3. **How do you check the version of Node.js installed on your system?**  
   By running the command:

   ```bash
   node -v
   ```

   This displays the currently installed version of Node.js.

4. **Can you run React without Node.js?**  
   While it is theoretically possible, it is not practical. Without Node.js, you cannot use npm or access React’s development tools, making the development process highly restrictive.

# Module

## Explanation

In Node.js, a module is a reusable block of code that provides specific functionalities. Modules can be included in your project using `require` or `import` statements.

### Types of Modules in Node.js:

1. **Core Modules**: Pre-installed modules like `fs`, `http`, etc.
2. **User-defined Modules**: Custom modules created by developers.
3. **Third-party Modules**: Modules installed using NPM (Node Package Manager).

### Real-life Example:

Core modules act like a pre-packed toolkit with tools like a hammer and screwdriver. You can also create your own tools (user-defined modules) for specific tasks.

---

## Why use Modules?

- Helps organize and reuse code.
- Prevents code conflicts between files.
- React projects heavily use modules to manage components and libraries.

### Real-life Example:

Imagine a library where books are divided into sections like science, history, and fiction. You take only the section you need. Similarly, modules help in keeping code organized and manageable.

---

## Example of Using a Module:

### Code:

```javascript
// Using a Core Module
const fs = require("fs"); // Core module

fs.writeFileSync("example.txt", "Hello, Node.js!"); // Creates a file with content
```

---

## Interview Questions:

1. **What is a module in Node.js?**  
   A module in Node.js is a reusable block of code that can include variables, functions, or objects. It can be imported or exported between files.

2. **What are the types of modules in Node.js?**

   - Core Modules: Built-in modules like `fs`, `http`.
   - User-defined Modules: Custom modules written by developers.
   - Third-party Modules: Modules downloaded using NPM.

3. **Why do we use modules in React projects?**  
   Modules help organize code into smaller, reusable pieces. React components are essentially modules, making it easier to manage and reuse them.

4. **How do you include a core module in a Node.js application?**  
   Use the `require` statement:
   ```javascript
   const http = require("http");
   ```

# Module

## Explanation:

In Node.js, a module is a reusable piece of code that provides specific functionalities. Modules can be imported and used in other files to avoid code duplication and keep the application organized.

## Types of Modules in Node.js:

1. **Core Modules**: Pre-installed modules like `fs`, `path`, `http`, etc.
2. **User-defined Modules**: Custom modules that you create for specific tasks.
3. **Third-party Modules**: Modules installed via npm, such as `express`, `lodash`, etc.

## Why Use Modules?

- **Code Organization**: Keeps your codebase clean and modular.
- **Reusability**: Write once, use multiple times.
- **Avoid Conflicts**: Encapsulation prevents code in one file from interfering with another.

## Real-life Example:

Core modules act like a toolkit that provides ready-made tools (e.g., hammer, screwdriver). Similarly, you can create user-defined tools for specific tasks.

### Example:

#### Core Module Usage with Modern ES6 Syntax

```javascript
import { writeFileSync } from "fs"; // Importing a core module

writeFileSync("example.txt", "Hello, Node.js!"); // Creates a file with the given content
```

#### User-defined Module

**math.js**:

```javascript
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
```

**app.js**:

```javascript
import { add, subtract } from "./math.js";

console.log(add(5, 3)); // Output: 8
console.log(subtract(5, 3)); // Output: 2
```

#### Third-party Module

Install a module using npm:

```bash
npm install lodash
```

Usage:

```javascript
import _ from "lodash";

const numbers = [10, 20, 30, 40];
const sum = _.sum(numbers);

console.log(sum); // Output: 100
```

## Interview Questions:

1. **What is a module in Node.js?**

   - A module is a reusable block of code encapsulated in a file. It can export variables, functions, or objects to be used in other files.

2. **What are the types of modules in Node.js?**

   - Core Modules
   - User-defined Modules
   - Third-party Modules

3. **How do you use modules in Node.js with modern ES6 syntax?**

   - Use the `import` and `export` keywords. Example:
     ```javascript
     import { writeFileSync } from "fs";
     writeFileSync("example.txt", "Hello, Node.js!");
     ```

4. **What is the difference between CommonJS and ES6 Modules?**
   - **CommonJS**: Uses `require` and `module.exports` (default in Node.js).
   - **ES6 Modules**: Uses `import` and `export` (modern JavaScript syntax).

### Package

#### Explanation:

In Node.js, a **package** is a file or a folder that provides a set of functionalities. Packages are managed via **npm (Node Package Manager)**.

**Example:** React is a package that provides tools for building UI components and designing interfaces.

#### Command to Create a Package:

To create a package, run the following command in your terminal:

```bash
npm init
```

Follow the prompts to generate a `package.json` file.

---

### What is a Package?

A package is a collection of modules that includes dependencies and metadata stored in a `package.json` file. Packages are used to incorporate pre-built solutions into projects, saving time and effort.

#### Why Use Packages?

- Speeds up development by providing ready-made solutions.
- Allows reuse of optimized and tested code.

---

### Example:

In a React project, you might use the `axios` package to fetch data from APIs.

```javascript
// Importing axios to fetch data from an API
import axios from "axios";

axios
  .get("https://jsonplaceholder.typicode.com/posts")
  .then((response) => console.log(response.data))
  .catch((error) => console.error(error));
```

---

### Real-life Example:

When you order pizza, it arrives as a package that includes the pizza, a box, and napkins. You get a ready-to-eat meal without needing to prepare each ingredient separately. Similarly, packages provide ready-to-use modules for coding.

---

### Interview Questions:

#### 1. What is the difference between a module and a package?

- A **module** is a single file containing reusable code.
- A **package** is a collection of modules along with metadata and dependencies.

#### 2. How do you create a module in JavaScript?

By exporting a function or variable:

```javascript
// file: myModule.js
export const greet = () => console.log("Hello!");
```

Then import it as:

```javascript
import { greet } from "./myModule.js";
greet(); // Output: Hello!
```

#### 3. What is the purpose of the `package.json` file?

- It stores project metadata such as dependencies, scripts, and project information.
- It helps npm manage the packages required by your project.

#### 4. How do you install a package using npm?

Run the following command in the terminal:

```bash
npm install <package-name>
```

#### 5. What are some common npm packages used in React?

- **react-router-dom**: For routing
- **axios**: For making API calls
- **redux**: For state management

# Node Package Manager (NPM)

## Explanation

NPM (Node Package Manager) is a tool that manages Node.js packages. It provides options to install, update, and remove dependencies using commands like `npm install`.

### Example Commands

- **Install React:**

  ```bash
  npm install react
  ```

- **Uninstall a package:**

  ```bash
  npm uninstall react
  ```

### Real-life Example

Imagine you have a library with various books (packages). NPM allows you to borrow (install) or return (uninstall) books based on your needs.

---

## What is NPM?

- **NPM** is a package manager that comes with Node.js.
- It is a tool to install packages for React, Express, and other JavaScript libraries and frameworks.

---

## Features of NPM

1. **Install packages:** Easily add third-party libraries and frameworks to your project.

   ```bash
   npm install <package-name>
   ```

2. **Manage dependencies:** Maintain a list and versions of libraries required for the project.
3. **Custom scripts:** Define custom commands for automation tasks.

### Real-life Example

A mall food court allows you to pick food from different stalls. NPM acts like the mall where you can get packages like React, Axios, and Bootstrap.

---

## How to Use NPM?

### Install Node.js

NPM comes bundled with Node.js. You can [download Node.js](https://nodejs.org/).

### Initialize NPM

To initialize a project and create a `package.json` file:

```bash
npm init
```

This file stores project metadata and dependencies.

### Install a Package Globally

For system-wide use:

```bash
npm install -g <package-name>
```

Example: Installing React Developer Tools globally.

### Install a Package Locally

For use only within the current project:

```bash
npm install <package-name>

```

# Create React App

## Method 1: Using Create React App (CRA)

### Step 1: Install Node.js

First, install Node.js. NPM (Node Package Manager) comes bundled with Node.js.

### Step 2: Create a New React App

Run the following command to create a React app:

```bash
npx create-react-app my-app
```

- `npx`: Node Package Runner that allows running packages without globally installing them.
- `my-app`: The name of your project.

Wait until all dependencies are installed.

### Step 3: Run the App

1. Navigate to the project directory:
   ```bash
   cd my-app
   ```
2. Start the development server:
   ```bash
   npm start
   ```
3. Open your browser and visit [http://localhost:3000](http://localhost:3000).

---

## Method 2: Using Vite

### Why Vite?

- **Faster builds**: Vite offers better performance than CRA.
- **Hot Module Replacement (HMR)**: Instantly updates changes.
- **Lightweight**: Works with minimal configuration.

### Step 1: Install Node.js

Ensure Node.js is installed.

### Step 2: Create a React App Using Vite

Run the following command:

```bash
npm create vite@latest my-vite-app
```

1. Select `React` and then choose `React + JavaScript` (or `TypeScript` if you prefer).
2. Move to the project directory:
   ```bash
   cd my-vite-app
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Step 3: Run the App

Start the development server:

```bash
npm run dev
```

Open your browser and visit [http://localhost:5173](http://localhost:5173).

---

## Method 3: Using Bun

### Why Bun?

- **Superfast installs**: Bun is significantly faster than NPM and Yarn.
- **Built-in tools**: Acts as a bundler and transpiler.
- **Efficient runtime**: Handles both JavaScript and TypeScript efficiently.

### Step 1: Install Bun

1. Install Bun from its official site: [Bun.sh](https://bun.sh).
2. Use this command to install:
   ```bash
   curl -fsSL https://bun.sh/install | bash
   ```

### Step 2: Create a React App Using Bun

Create a new React app:

```bash
bun create react my-bun-app
```

1. Move to the project directory:
   ```bash
   cd my-bun-app
   ```

### Step 3: Run the App

Start the development server:

```bash
bun dev
```

Open your browser and visit [http://localhost:3000](http://localhost:3000).

---

## Comparison: CRA vs Vite vs Bun

| Feature                    | CRA               | Vite        | Bun               |
| -------------------------- | ----------------- | ----------- | ----------------- |
| **Speed**                  | Slow              | Fast        | Fastest           |
| **Configuration**          | Minimal           | Minimal     | Minimal           |
| **Hot Module Replacement** | Supported         | Superfast   | Superfast         |
| **Bundling**               | Webpack           | ESBuild     | Bun's Built-in    |
| **Use Case**               | Beginner-friendly | Modern apps | Performance focus |

---

## Interview Questions

1. **What is Create React App (CRA)? Why is it used?**

   - CRA is a boilerplate tool that provides a ready-to-use structure for creating React applications.

2. **Why should you consider using Vite over CRA?**

   - Vite offers faster builds and better HMR, making it more efficient for large-scale applications.

3. **What is Bun, and how does it differ from NPM?**

   - Bun is a JavaScript runtime that is significantly faster than NPM and Yarn, and it provides built-in tools.

4. **What is the default port for CRA and Vite?**

   - CRA: [http://localhost:3000](http://localhost:3000)
   - Vite: [http://localhost:5173](http://localhost:5173)

5. **How do you start a React project using Bun?**

   ```bash
   bun create react <app-name>
   cd <app-name>
   bun dev

   ```

# Visual Studio Code (VS Code)

## What is VS Code?

Visual Studio Code ek lightweight aur powerful code editor hai jo React aur JavaScript projects ke liye perfect hai.

## Features of VS Code:

- **Extensions**: Tum alag-alag extensions add kar sakte ho jaise Prettier, ESLint, aur React snippets.
- **IntelliSense**: Code suggestions aur auto-complete feature provide karta hai.
- **Built-in terminal**: Direct terminal access milta hai, jo NPM commands run karne ke kaam aata hai.
- **Debugger**: Tum code ko debug kar sakte ho errors ko identify karne ke liye.

## Real-life example:

VS Code ek Swiss Army knife ki tarah hai jo sab tools ek hi jagah provide karta hai—coding, debugging, aur project management ke liye.

## Important Extensions:

- **ESLint**
- **Prettier**
- **React Developer Tools**

## How to Set Up VS Code for React Development?

### 1. Download and Install:

Download VS Code from the official website and install it.

### 2. Install Extensions:

- **ES7+ React/Redux/GraphQL/React-Native Snippets**: React ke shortcuts ke liye.
- **Prettier - Code formatter**: Code clean aur readable banane ke liye.
- **Bracket Pair Colorizer 2**: Code blocks ko clearly identify karne ke liye.

### 3. Configure Settings for Better Workflow:

Settings mein `formatOnSave` enable karo:

Go to Settings ⚙️ > Search for "Format On Save" > Enable it.

# React Boilerplate and Styles in JSX

In this section, we will learn about React Boilerplate and Styles in JSX in detail.

## 1. React Boilerplate

React Boilerplate provides a basic structure commonly used in React projects. Its goal is to provide a clean and organized setup for starting React development.

### Basic React Boilerplate Structure

When you use tools like Create React App, Vite, or Bun, a typical folder structure looks like this:

```plaintext
my-app/
├── node_modules/            # Dependencies
├── public/
│   ├── index.html           # Main HTML file
│   └── favicon.ico          # Favicon
├── src/
│   ├── assets/              # Images, videos, fonts
│   ├── components/          # Reusable components (e.g., Header, Footer)
│   ├── App.js               # Main App Component
│   ├── index.js             # Entry point of the React app
│   └── styles.css           # Global styles
├── .gitignore               # Git ignore file
├── package.json             # Project configuration file
└── README.md                # Project documentation
```

### Important Files

- **index.html (in `public/`)**: This file loads the React app. It contains `<div id="root"></div>` where the React app is rendered.
- **index.js (in `src/`)**: This is the entry point for the React app. It initializes React and renders `App.js` into the root div.
- **App.js (in `src/`)**: This is the main component of the React app where all components are organized.

---

## 2. Styles in JSX

React supports inline styles and CSS-in-JS for styling components. Styles written directly within JSX are called "Styles in JSX."

### Inline Styles

Inline styles in React are written as JavaScript objects, where CSS properties are written in camelCase (e.g., `backgroundColor` instead of `background-color`).

#### Example: Inline Styles in JSX

```jsx
import React from "react";

function App() {
  const headerStyle = {
    color: "blue",
    fontSize: "40px",
    textAlign: "center",
  };

  return (
    <div>
      <h1 style={headerStyle}>Welcome to React</h1>
      <p>This is a sample React app with inline styling.</p>
    </div>
  );
}

export default App;
```

- **`headerStyle`**: A JavaScript object applied to the `h1` element.
- CSS properties must be written in **camelCase**.

### CSS-in-JS Libraries (e.g., Styled Components)

For complex styles, you can use libraries like `styled-components` to encapsulate styles within components.

#### Example: Using Styled Components

First, install the library:

```bash
npm install styled-components
```

Then, create styled components:

```jsx
import React from "react";
import styled from "styled-components";

const Header = styled.h1`
  color: blue;
  font-size: 40px;
  text-align: center;
`;

function App() {
  return (
    <div>
      <Header>Welcome to React</Header>
      <p>This is a sample React app with styled-components.</p>
    </div>
  );
}

export default App;
```

- **Styled Components**: Styles are directly defined in the component.

---

## Injecting Data into JSX Elements

In React, you can inject dynamic data into JSX using curly braces `{}`. This allows you to insert JavaScript variables, expressions, or functions into HTML elements.

#### Example: Injecting Data into JSX

```jsx
import React from "react";

function App() {
  const name = "Amit Mishra";
  const age = 25;
  const isMember = true;

  return (
    <div>
      <h1>{`Hello, ${name}`}</h1>
      <p>{`Age: ${age}`}</p>
      <p>{isMember ? "Member" : "Not a Member"}</p>
    </div>
  );
}

export default App;
```

- **Curly Braces `{}`**: Used to inject JavaScript variables into JSX.
- **Conditional Rendering**: `isMember` checks and displays either "Member" or "Not a Member."

---

## 3. Exercises on React Boilerplate & Styles in JSX

### Exercise 1: Basic React App with Inline Styling

1. Create a simple React app with a header styled in blue.
2. Add a paragraph that injects a dynamic `name` variable.

### Exercise 2: Creating a Styled Component

1. Install `styled-components`.
2. Create a component with styles defined inside the component using `styled-components`.

---

## Interview Questions: React Boilerplate & Styles in JSX

### 1. What is the folder structure of a typical React app?

- **Answer**: The typical structure includes:
  - `public/` folder with `index.html`.
  - `src/` folder with React components and entry files like `App.js` and `index.js`.
  - `package.json` for dependencies.

### 2. How do you apply inline styles in React?

- **Answer**: Inline styles are written as a JavaScript object with properties in camelCase.
  ```jsx
  const style = { color: "blue" };
  <h1 style={style}>Hello</h1>;
  ```

### 3. What are styled-components in React?

- **Answer**: Styled-components is a library that allows defining styles directly in React components, encapsulating styles within the component.

### 4. Why would you use JSX to inject data?

- **Answer**: JSX allows injecting dynamic data like variables, expressions, and functions into elements, making it easier to render dynamic content. This is done using `{}` syntax.

# Create React App

## Method 1: Using Create React App (CRA)

### Step 1: Install Node.js

First, install Node.js. NPM (Node Package Manager) comes bundled with Node.js.

### Step 2: Create a New React App

Run the following command to create a React app:

```bash
npx create-react-app my-app
```

- `npx`: Node Package Runner that allows running packages without globally installing them.
- `my-app`: The name of your project.

Wait until all dependencies are installed.

### Step 3: Run the App

1. Navigate to the project directory:
   ```bash
   cd my-app
   ```
2. Start the development server:
   ```bash
   npm start
   ```
3. Open your browser and visit [http://localhost:3000](http://localhost:3000).

---

## Method 2: Using Vite

### Why Vite?

- **Faster builds**: Vite offers better performance than CRA.
- **Hot Module Replacement (HMR)**: Instantly updates changes.
- **Lightweight**: Works with minimal configuration.

### Step 1: Install Node.js

Ensure Node.js is installed.

### Step 2: Create a React App Using Vite

Run the following command:

```bash
npm create vite@latest my-vite-app
```

1. Select `React` and then choose `React + JavaScript` (or `TypeScript` if you prefer).
2. Move to the project directory:
   ```bash
   cd my-vite-app
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Step 3: Run the App

Start the development server:

```bash
npm run dev
```

Open your browser and visit [http://localhost:5173](http://localhost:5173).

---

## Method 3: Using Bun

### Why Bun?

- **Superfast installs**: Bun is significantly faster than NPM and Yarn.
- **Built-in tools**: Acts as a bundler and transpiler.
- **Efficient runtime**: Handles both JavaScript and TypeScript efficiently.

### Step 1: Install Bun

1. Install Bun from its official site: [Bun.sh](https://bun.sh).
2. Use this command to install:
   ```bash
   curl -fsSL https://bun.sh/install | bash
   ```

### Step 2: Create a React App Using Bun

Create a new React app:

```bash
bun create react my-bun-app
```

1. Move to the project directory:
   ```bash
   cd my-bun-app
   ```

### Step 3: Run the App

Start the development server:

```bash
bun dev
```

Open your browser and visit [http://localhost:3000](http://localhost:3000).

---

## Comparison: CRA vs Vite vs Bun

| Feature                    | CRA               | Vite        | Bun               |
| -------------------------- | ----------------- | ----------- | ----------------- |
| **Speed**                  | Slow              | Fast        | Fastest           |
| **Configuration**          | Minimal           | Minimal     | Minimal           |
| **Hot Module Replacement** | Supported         | Superfast   | Superfast         |
| **Bundling**               | Webpack           | ESBuild     | Bun's Built-in    |
| **Use Case**               | Beginner-friendly | Modern apps | Performance focus |

---

## Interview Questions

1. **What is Create React App (CRA)? Why is it used?**

   - CRA is a boilerplate tool that provides a ready-to-use structure for creating React applications.

2. **Why should you consider using Vite over CRA?**

   - Vite offers faster builds and better HMR, making it more efficient for large-scale applications.

3. **What is Bun, and how does it differ from NPM?**

   - Bun is a JavaScript runtime that is significantly faster than NPM and Yarn, and it provides built-in tools.

4. **What is the default port for CRA and Vite?**

   - CRA: [http://localhost:3000](http://localhost:3000)
   - Vite: [http://localhost:5173](http://localhost:5173)

5. **How do you start a React project using Bun?**

   ```bash
   bun create react <app-name>
   cd <app-name>
   bun dev

   ```

# Exercises: Level 1

## 1. Display an Image in React

**Objective:** Import an image from the `src/` folder and display it in your React component.

**Instructions:**

- Import an image in your React component using `import`.
- Render the image using the `<img>` tag.

```jsx
import React from "react";
import logo from "./logo.png"; // Replace with the correct path

function App() {
  return (
    <div>
      <img src={logo} alt="Logo" />
    </div>
  );
}

export default App;
```

## 2. Display Your Name with Dynamic Data in JSX

Objective: Inject dynamic data (string) into JSX and display it in your app.

Instructions:

Create a variable that stores your name.
Render the name in JSX.

```jsx
import React from "react";

function App() {
  const name = "Amit Mishra"; // Dynamic data
  return (
    <div>
      <h1>{name}</h1> {/* Injecting dynamic data */}
    </div>
  );
}

export default App;
```

# Exercises: Level 2

## 1. Use Audio or Video in React

Objective: Import an audio or video file and display it using the appropriate HTML tags.

Instructions:

Import an audio or video file.
Render the <audio> or <video> tag with the media file.

```jsx
import React from "react";
import myAudio from "./audio.mp3"; // Replace with correct path

function App() {
  return (
    <div>
      <audio controls>
        <source src={myAudio} type="audio/mp3" />
        Your browser does not support the audio element.
      </audio>
    </div>
  );
}

export default App;
```

2. Implement a Custom Font in React
   Objective: Use a custom font from Google Fonts.

Instructions:

Import a font from Google Fonts in your index.html or CSS file.
Apply the font to your component.

```jsx
import React from "react";
import "./App.css"; // Import the CSS file

function App() {
  return (
    <div>
      <h1 className="custom-font">Hello, World!</h1>
    </div>
  );
}

export default App;
```

In App.css:

```css
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

.custom-font {
  font-family: "Roboto", sans-serif;
}
```

# Exercises: Level 3

## 1. Create a Responsive Layout with Images and Media

Objective: Build a small layout using images and media files that is responsive.

Instructions:

Use images, videos, and audio in a responsive layout.
Make sure the layout adapts to different screen sizes.

```jsx
import React from "react";
import logo from "./logo.png";
import myVideo from "./video.mp4";

function App() {
  return (
    <div style={{ padding: "20px" }}>
      <h1>My Media Gallery</h1>
      <div
        style={{
          display: "flex",
          flexDirection: "column",
          alignItems: "center",
        }}
      >
        <img
          src={logo}
          alt="Logo"
          style={{ width: "50%", marginBottom: "20px" }}
        />
        <video width="320" height="240" controls>
          <source src={myVideo} type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>
    </div>
  );
}

export default App;
```

## 2. Build a Gallery with Multiple Media Types

Objective: Create a small gallery using a combination of images, videos, and audio files.

Instructions:

Create a component that renders multiple media files (images, videos, and audio) in a gallery style.
Use flexbox or grid to organize the media in rows and columns.

```jsx
import React from "react";
import logo from "./logo.png";
import myAudio from "./audio.mp3";
import myVideo from "./video.mp4";

function App() {
  return (
    <div style={{ padding: "20px" }}>
      <h1>Media Gallery</h1>
      <div
        style={{
          display: "grid",
          gridTemplateColumns: "repeat(3, 1fr)",
          gap: "20px",
        }}
      >
        <img src={logo} alt="Logo" style={{ width: "100%" }} />
        <audio controls style={{ width: "100%" }}>
          <source src={myAudio} type="audio/mp3" />
          Your browser does not support the audio element.
        </audio>
        <video width="100%" controls>
          <source src={myVideo} type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </div>
    </div>
  );
}

export default App;
```

# Interview Questions

How do you import images and media files in React?
You can import images or media files from the src/ folder using import, or from the public/ folder by referencing the file path directly.

How do you add custom fonts in React?
Custom fonts can be added by importing them through a <link> tag in index.html or by using @import in a CSS file. Then, you apply the font to elements using CSS.

What is the benefit of using public/ folder for media files?
Media files in the public/ folder can be accessed via URL directly, and they won’t be bundled by Webpack, which may be useful for static assets.

How do you make media elements responsive in React?
You can use inline styles or CSS media queries to make media elements responsive. For example, setting width: 100% for images or videos allows them to adjust according to the screen size.
