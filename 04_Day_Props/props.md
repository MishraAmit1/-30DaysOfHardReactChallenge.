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
<small> December 24, 2024</small>
</sub>

</div>

[<< Day 1](../01_Day_Introduction_To_React/README.md) | [Day 3 >>](../03_Day_Setting_Up/README.md)

![30 Days of Hard React banner](../images/banner.webp)

# React Props: Zero to Hero

## **Table of Contents**

- [Props](#props)
  - [Props in Functional Component](#props-in-functional-component)
  - [What is props?](#what-is-props)
  - [Props Object](#props-object)
  - [Different Data Type Props](#different-data-type-props)
    - [String Props Type](#string-props-type)
    - [Number Props Type](#number-props-type)
    - [Boolean Props Type](#boolean-props-type)
    - [Array Props Type](#array-props-type)
    - [Object Props Type](#object-props-type)
    - [Function Prop Types](#function-prop-types)
  - [Destructuring Props](#destructuring-props)
  - [defaultProps](#defaultprops)
- [Exercises: Components and Props](#exercises-components-and-props)
  - [Exercises: Level 1](#exercises-level-1)
  - [Exercises: Level 2](#exercises-level-2)
  - [Exercises: Level 3](#exercises-level-3)

---

## **Props**

### **Props in Functional Component**

Props in React are short for "properties." They allow you to pass data from a parent component to a child component in a reusable and dynamic way.

---

### **What is props?**

- Props are **read-only** and help make components reusable by receiving data as input.
- They follow a **unidirectional data flow** (from parent to child).

---

### **Props Object**

All props are passed as a single object called the `props` object.

```jsx
function Child(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  return <Child name="Amit" />;
}
```

### **Different Data Type Props**

### **String Props Type**

Pass strings as props.

```jsx
function Greeting({ message }) {
  return <h1>{message}</h1>;
}

function App() {
  return <Greeting message="Hello, World!" />;
}
```

### **Number Props Type**

Pass numbers as props.

```jsx
function AgeDisplay({ age }) {
  return <p>Age: {age}</p>;
}

function App() {
  return <AgeDisplay age={25} />;
}
```

### **Boolean Props Type**

Pass true/false as props.

```jsx
function Status({ isActive }) {
  return <p>Status: {isActive ? "Active" : "Inactive"}</p>;
}

function App() {
  return <Status isActive={true} />;
}
```

### **Array Props Type**

Pass arrays as props.

```jsx
function Items({ list }) {
  return (
    <ul>
      {list.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
}

function App() {
  return <Items list={["Apple", "Banana", "Cherry"]} />;
}
```

### **Object Props Type**

Pass objects as props.

```jsx
function Profile({ user }) {
  return (
    <h2>
      {user.name}, {user.age}
    </h2>
  );
}

function App() {
  const user = { name: "Amit", age: 25 };
  return <Profile user={user} />;
}
```

### **Function Prop Types**

Pass functions as props.

```jsx
function Button({ onClick }) {
  return <button onClick={onClick}>Click Me</button>;
}

function App() {
  const handleClick = () => alert("Button clicked!");
  return <Button onClick={handleClick} />;
}
```

### **Destructuring Props**

Instead of using props.property, destructure props for cleaner code.

```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}
```

### **defaultProps**

defaultProps sets default values for props.

```jsx
function Greeting({ message = "Hello, Reacts" }) {
  return <h1>{message}</h1>;
}

function App() {
  return <Greeting message="Hello, World!" />;
}
```

### **Exercises: Components and Props**

### **Exercises: Level 1**

Create a Greeting component that accepts a name prop and displays "Hello, [name]!"
Pass a number as a prop to a component and display it.
Pass a boolean prop to a component and conditionally render based on its value.

### **Exercises: Level 2**

Create a Profile component that accepts props for name, age, and bio and displays a user profile card.
Use the defaultProps feature to set default values for props.
Validate prop types for a Button component using propTypes.

### **Exercises: Level 3**

Build a TodoList component that takes an array of todo items as props and displays them as a list.
Create a parent component that passes a callback function as a prop to a child component.
Build a Gallery component that takes an array of image URLs as props and displays them in a grid.

## 🎉 CONGRATULATIONS! You have mastered React Props! 🎉
