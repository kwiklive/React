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



  
  
  


