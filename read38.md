## Conditional Rendering
 

Conditional rendering in React works the same way conditions work in JavaScript - you can use operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

 

```
function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}
```


- create a Greeting component that displays either of these components depending on whether a user is logged in:
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {    return <UserGreeting />;  }  return <GuestGreeting />;}
const root = ReactDOM.createRoot(document.getElementById('root')); 
// Try changing to isLoggedIn={true}:
root.render(<Greeting isLoggedIn={false} />);
 
 

## Conditional rendering is the process to show components based on a particular condition. For example, developers should show a task only if any pending task is available otherwise they can show a message like "There is no pending task available".

 

### Method 1: Inline if-else conditional (ternary) operator
Programmers can use the ternary operator ( ? : ) as a short if-else statement. The ternary operator is a simple javascript operator which takes 3 operands. 

Syntax:

While working with the ternary operator, developers need to wrap the whole expression in curly braces. To improve the readability of the code, users can wrap the operands inside the parenthesis. 

 

{
  condition ? ("condition is true") : ("condition is false")

- When the condition is true, it returns “condition is true” otherwise it returns “condition is false“.  Here, developers can include components as an operand instead of an HTML element.

Example:

Now, edit the App.js file and add the below code to it.

Filename: App.js

In this file, we will declare a variable name ‘totalTask’ and assign a value to this. Next, we will use the ternary operator to show the different messages according to the value of the ‘totalTask‘ variable

```
import React, { Component } from 'react';
 
// rendering different message according to the
// value of total task variable
class App extends Component {
  render() {
    const todoList = ['write article', 'read article', 'Review article'];
    const totalTask = todoList.length;
    return (
      <div>
        <h1 style={{color: "green"}}>GeeksForGeeks</h1>
         <b>{totalTask > 0 ?
         (<h2>The user has total {totalTask} task pending</h2>) :
         (<h2>The user has not any task pending</h2>) }</b>      
      </div>
    );
  }
}
  
export default App;

```
-- 
Command to run: 

`npm start`
 

 

### Method 2: Inline If with Logical && Operator
 

- Syntax:

Developers need to embed expression with the curly braces. If they need, they can wrap operands inside the parenthesis to keep the code clean. 

```
{
   (condition) && (React component or HTML code)
}
```


When the condition evaluates True, It returns the right part (react component or HTML code) as an output…

import React, { Component } from 'react';

// using inline if with logical && operator
```
class App extends Component {
render() {
    const todoList = [];
    const totalTask = todoList.length;
    return (
    <div>
        <h1 style={{color: "green"}}>GeeksForGeeks</h1>
      {
        (totalTask > 0) &&
        (<h2>The user has total {totalTask} task pending</h2>)
        }
        {
        (totalTask === 0) &&
        (<h2>The user has not any pending task.</h2>)
        }    
    </div>
    );
}}
export default App;
```


- If with Logical && Operator which works the same in React as it works in Javascript. It takes 2 conditions as operands, if the first condition is True, it only evaluates the second condition. Method 2: Instead of adding condition as a second operand, we can add react component. We can use this to wrap operands inside parenthesis to keep the code clean.

 

 

## List and keys in React intro
In this article, I explain what lists are, how to build a list in JSX, what keys are and how to fix one of the most common errors connected to list and keys. This article will be a complete cheat sheet about lists and keys in React, so make sure you'll save it in your favorites to come back when you need to remind something.

 

- The .map() method in Javascript. calls a function on every element of that array. Then it creates a new array with transformed values. It doesn't change the parent array. Let's imagine that you are creating a simple Todo App.

The main element of your project will be a list of tasks. To show them, you will need data, which in most cases will be an array of elements.

 

```
const tasks = [
  {text: "Buy flowers", status: "todo"},
  {text: "Go to the dentist", status: "done"},
]

const tasksList = tasks.map(task => {
  return (
  <p>{task.text} - {task.status}</p>
  ```

## key


key is a special attribute that you need to include in the element, 
and it should be a string. Keys in each list should be unique, which means 
you shouldn't use values that can be the same as the key. For example, you should not use status or text as a key in our example. It helps React to identify which element was changed, added, or removed.

key is a special attribute that you need to include in the element, and it should be a string. Keys in each list should be unique, 
which means you shouldn't use values that can be the same as the key. For example, you should not use status or text as a key in our example. 
It helps React to identify which element was changed, added, or removed.   )


```
const tasks = [
  {id: "1", text: "Buy flowers", status: "todo"},
  {id: "3", text: "Go to the dentist", status: "done"},
]

const tasksList = tasks.map(task => {
  return (
  <p key={task.id}>{task.text} - {task.status}</p>
  )
});
```