# React

## What is React?
- React is a JavaScript library for building user interfaces.
- React is used to build single-page applications.
- React allows us to create reusable UI components.
- React, sometimes referred to as a frontend JavaScript framework. 
- React is light weight and fast.
- React offers One way data binding, parent sends response to children.



## Note
- React does not understand HTML. 
- It understands JSX only which is HTML + JS.
- JSX content must have one and only one parent. i.e. all the JSX content must be under a div finally.


## Who is behind React?
React is a JavaScript library created by Facebook and its first public release was in July 2013..

## How does React Work?
Instead of manipulating the browser's DOM directly, React creates a virtual DOM (copy of the actual DOM) in memory, where it does all the necessary manipulating, before making the changes in the browser DOM.

React finds out what changes have been made, and changes only what needs to be changed.

## React Installation/Environment
- Install Node.js
- Install create-react-app

Raect can be included in HTML through its CDN to learn without installation. 

## VSCode Extensions
Usefull VSCode extension to help React programming

- VS Code ES7+ React/Redux/React-Native/JS snippets (dsznajder)

## Creating a react app
Open terminal or VSCode at folder where React project is to be created.
> create-react-app app-name

or

> npx create-react-app app-name

## Starting a react app
Go to application folder first, then;
> npm start

A new browser window will pop up with your newly created React App! If not, open your browser and type localhost:3000 in the address bar.

## Where we work in React
1. We dont work on 'public/index.html' file.
2. We create components say in the 'Components' folder.
3. We import those components on 'src/App.js' file.
4. This component is displayed through index.js file.


## React Components
- Components are independent and reusable bit of code.
- They serve same function as JS files.
- They work in isolation and return HTML via a render function.
- If we talk about a webpage, following are good candidates for components: Header, Navigation, SideMenu, Featured Product, Blog, Contact Form, Button, Footer.

React is a component based library. It enables to divide our UI in smaller reusable components. Let we have a 'Call to Action' UI component with a text and button. It will have same layout, colors style and structure for all the services except text and the button. These two will change for a service. This we achieve with props.


### Class Based Components
- It is actually an ES6 class.
- We use it to manage states, Private Object or Data. 
- It can recieve props/arguments optionally and returns HTML.

### Functional Components
- These are mainly used to create UI.
- These are actually javascript functions.
- Receives props optionally.
- It returns JSX always.

### Creating a Class Based React Component
1. Let there will be a folder to keep components. So if not already created, create a folder 'Components' under ‘src'.
2. Let Component name is Blog so create a file Blog.js under folder Components.
3. On Blog.js file add this code for an example:

````
import React, {Component} from ‘react’;

class Blog extends Component
{

  // Constructor will be added here
  
  // Render
	render() {
		
		return(
            <div>
                <div>Title: React is the Best</div>
                <div>Category: Web Programming</div>
            </div>
		) 
	}

}

export default Blog;
````


### Creating a Function Based React Component
1. Let there will be a folder to keep components. So if not already created, create a folder 'Components' under ‘src'.
2. Let Component name is Blog so create a file Blog.js under folder Components.
3. On Blog.js file add this code for an example:

````
import React from ‘react’;

function Blog()
{
	return(
                <div>Title: React is the Best</div>
                <div>Category: Web Programming</div>
	) 

}

export default Blog;
````

We can write a functional component with arraow function also.

````
import React from ‘react’;

const Blog = () =>
{
	return(
                <div>Title: React is the Best</div>
                <div>Category: Web Programming</div>
	) 

}

export default Blog;
````

Above functions can be imported in any name. But if we want named export only, then write function this way. Now it will be used by name Blog only, not 'B' or anything else.


````
import React from ‘react’;

export const Blog = () =>
{
	return(
                <div>Title: React is the Best</div>
                <div>Category: Web Programming</div>
	) 

}

````

### Creating a functional component with VSCode ES7 Extension
**Function Type and Keyword**
React Functional Component = *rfc*
React Functional Component with Export = *rfce*

React Arrow Functional Component = *rafc*
React Arrow Functional Component with Export = *rafce*

Just type the keyword and press the tab to get a ready to modify function.

## JSX
- JSX is an extension to Javascript Language Syntax.
- JSX = JavaScript + XML
- JSX contain HTMLlike attributes. HTML attributes also work under JSX.
- JSX requires every tag to be closd.
- JSX requires a parent element above the content.

// We can use React.createElement() instead of JSX to render HTML. But it is preferred to use JSX because React.createElement is difficult and lengthy to write.


## Props (Properties)
Props are properties and allows to send data from one component to other. It works one way and follow a uni-directional flow i.e, parent to child only. Props helps to make a component dynamic.

Props are objects actually.

### Passing props to class based component

Code example in App.js

````  
return (
    <div className='App'>
      <Person name="Adam" />
      <Person name="Brave" age="20"/>
    </div>
  );
````

Example Component file

````

import React, { Component } from 'react'

class User extends Component{

    constructor(props){
         super(props);
         this.props = props;
     }

    render(){

        return(
            <div>
                <div>My name is: { this.props.name }</div>
                <div>My age is: {this.props.age} years</div>
            </div>
        )

    }

}

export default Person;

````

Result

My name is: Adam

My age is: Years

My name is: Brave

My age is: 20 Years

Note that, when props is not available it just keeps the blank instead of showing any error.

## State
State is an in-built object in the class based componnets. Function based components are stateless. Hooks are used in functions based components to use the state.

State is treated as component specific private data and only accessible inside the component it belongs to. It is not accessible to any other class or anywhere else.

State is mutable and can be changed as per requirement.
State 'state holds' the data for the component.  To access this data, it need to be sent with the help of props.

### How to use state
1. In class base components: this.state
2. In functions base components: useState. (This is a hook)

### How to create state
In App.js

````
function App() {
  return (
    <div className='App'>
      <User />
    </div>
  );
}
````

In User.js. (It is class based component)

**Add following to constructor:**

````
         this.state = {
            name: "Bob",
            age: 24
         }

````

**Add following as return function under render**

````
        return(
            <div>
                <div>User name : {this.state.name}</div>
                <div>User's age is: {this.state.age} years</div>
            </div>
        )

````


### How to change state & re-render (State Mutation)

In User.js. (It is class based component)

**Add following to constructor:**

````
         this.state = {
            name: "Bob",
            age: 24
         }
	 
     changeState = () => {
        this.setState({
            name: "Alex",
            age: 35
        });
     }
	 

````

**Add a button with onClick event...**

````
        return(
            <div>
                <div>User name : {this.state.name}</div>
                <div>User's age is: {this.state.age} years</div>
		<br/>
		<button onClick={this.changeState.bind(this)}>Change State</button>
            </div>
        )

````
We use arrow function here. Using simple function is not good because 'this' keyword gets rebind. But if really want to use simple function here we can achieve the result using event binding methods.

**Method 1**

````
<button onClick={() => this.changeState()}>Change State</button>
````

**Method 2: Inline Binding**

````
<button onClick={this.changeState.bind(this)}>Change State</button>
````

**Method 3: Inline Binding**
Simply write like this and binding will happen under constructor.

````
<button onClick={this.changeState}>Change State</button>
````


````
this.state={};
.....

this.changeState = this.changeState.bind(this);

````

**Method 4**
We used already. We wrote this:

````
<button onClick={this.changeState.bind(this)}>Change State</button>
````

with arrow function binding.

````
     changeState = () => {
        this.setState({
            name: "Alex",
            age: 35
        });
     }

````
