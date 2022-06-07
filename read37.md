# React 1

- React is a JavaScript library

## Introducing JSX

`const element = <h1>Hello, world!</h1>;`

- JSX is a JavaScript Extension Syntax used in React to easily write HTML and JavaScript together.

## Why JSX 


- Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called "components" that contain both. We will come back to components in a further section, but if you're not yet comfortable putting markup in JS, this talk might convince you otherwise.

`const jsx = <h1>This is JSX</h1>`

This is simple JSX code in React. But the browser does not understand this JSX because it's not valid JavaScript code. This is because we're assigning an HTML tag to a variable that is not a string but just HTML code.

So to convert it to browser understandable JavaScript code, we use a tool like Babel which is a JavaScript compiler/transpiler.

What is the React.createElement Function?
Every JSX is converted to the React.createElement function call that the browser understands.

The React.createElement has the following syntax:

React.createElement(type, [props], [...children])
Let’s look at the parameters of the createElement function.

type can be an HTML tag like h1, div or it can be a React component
props are the attributes you want the element to have
children contain other HTML tags or can be a component
The React.createElement call will also be converted to the object representation like this:

```
{   
 type: 'h1',   
 props: {     
   children: 'This is JSX'   
 }
}
```
You can see this object representation if you assign the JSX to some local variable and log it as shown below:

```
class JSXDemo extends React.Component {
    render() {
        const jsx = <h1>This is JSX</h1>;
        console.log(jsx);
        return jsx;
    }
    }
```

ReactDOM.render(<JSXDemo />, document.getElementById('root'));
Here's a Code Sandbox Demo.

You will see the log printed as shown below:

log
Now, take a look at the below code:

```
class JSXDemo extends React.Component {
  render() {
    const jsx = <h1 id="jsx">This is JSX</h1>;
    console.log(jsx);
    return jsx;
  }
}
```

ReactDOM.render(<JSXDemo />, document.getElementById("root"));
Here, we've used the JSX like this:

'<h1 id="jsx">This is JSX</h1>
'So React, will convert this JSX to the below code:

`React.createElement("h1", { id: "jsx" }, "This is JSX");`

## Rendering an Element into the DOM


We call this a 'root' DOM because everything inside it will be managed by React DOM. Apps built with just React usually have a single root DOM node, but this can vary from application to application depending on the type of framework being used.

```
const root = ReactDOM.createRoot(
  document.getElementById('root')
);
const element = <h1>Hello, world</h1>;
root.render(element);
```


