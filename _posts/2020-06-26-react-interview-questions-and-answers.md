---
title: "React Interview Questions and Answers"
categories: [React]
tags: [React, React Interview]
---

## React Interview Questions and Answers

1) **General** React
* What is React? 
  - Frontend JavaScript library
  - Developed by Facebook in 2011
  - Follows **component** based approach
  - It allows to create **reusable** UI components
  - Used to develop complex, interactive web as well as mobile UI
  - Open-sourced in 2015 and has strong foundation and large community

* What are the features of React?
  - Uses **Virtual DOM**
  - Does **Server-side rendering**
  - Follows **Uni-directional data flow** i.e one way data binding

* List some of the major advantages of React.
  - Increases application performance
  - Can be used on client as well as server side
  - Readability is improved
  - **Easy to integrate**
  - Easy to write UI test cases

* What are the limitations of React?
  - **Not** a full sacle framework i.e just the **view**
  - Library is quite large
  - Difficult to understand for novice programmers
  - Uses inline templating and JSX

* What is JSX?
  - JSX stands for JavaScript XML
  - Utilizes the expressivess of JavaScript with a HTML - like template syntax
  - Makes HTML easy to understand
  - It is Robust
  - Boots up the JS performance
  - JSX expression must have only **one outermost element**

* What do you understand by Virtual DOM? Explain its working.
  - Lightweight JavaScript object which is the copy of the real DOM.
  - It works in 3 simple steps:
    * Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.
    * Then the difference between the previous DOM representation and the new one is calculated.
    * Once the calculations are done, the real DOM will be updated with only the things that have actually changed.
    ![Virtual_DOM_and_Real_DOM](https://user-images.githubusercontent.com/32950391/85906189-8bd60000-b7db-11ea-9948-6761b388f9f4.JPG)

* Differentiate between Real DOM and Virtual DOM.

| Virtual DOM						| Real DOM									|
| --- 								| ---										|
| 1. Updates faster					| 1. Updates Slower							|
| 2. Can't directly update HTML		| 2. Can directly update HTML				|
| 3. Updates if JSX element renders	| 3. If elements updates creates a new DOM	|
| 4. No DOM manipulation expense	| 4. DOM manipulation is very expensive		|
| 5. No memory wastage				| 5. Too much of memory wastage				|

* Why browsers can't read JSX?
  - JSX is not a regular JavaScript.
  - Browsers can read javaScript objects only.
  - JSX file is converted to JS object by JSX Transformer like Babel, before reaching Browser.
  ![JSX_File_Transformer_Javascript_Object](https://user-images.githubusercontent.com/32950391/85906835-8ed1f000-b7dd-11ea-8d56-ef05aadf0606.JPG)

* How React syntax changed from ES5 to ES6?
  - ES5
```javascript
var MyComponent = React.createClass({
	display : functioin () {..} ,
	render : function () {
		return (
			<div>
				<h1>Hello</h1>
			</div>
		);
	}
});
```

  - ES6
```javascript
class MyComponent extends React.Component{
	show() {..}
	render() {
		return(
			<div>
				<h1>Hello</h1>
			</div>
		);
	}
}
```

* How React is different from Angular?

| React				| TOPIC			| Angular			|
| :---:				| :---:			| :---:				|
| View				| Architecture	| MVC				|
| SSR				| Rendering		| CSR				|
| Virtual DOM		| DOM			| Real DOM			|
| One Way Binding	| Data Binding	| Two Way Binding	|
| Compile Time		| Bebugging		| Run Time			|
| Facebook			| Author		| Google			|


2) React **Components**
* What do you understand from 'In React, everything is a component'?
  - Components are **building blocks** of React application's UI
  - Components splits the UI into **independent, reusable** pieces, and renders each piece independently
  - JavaScript functions which takes in arbirary inputs and return HTML representation
  ![React_Components](https://user-images.githubusercontent.com/32950391/85911451-4e7d6c80-b7f3-11ea-8d33-f6ebd12193e2.JPG)

* Explain the purpose of **render()** in React.
  - Every component must have a **render()**
  - It returns **single React element** which is the representation of native DOM component
  - HTML elements inside render() must be enclosed inside an enclosing tag like <div>, <group>, <form> etc
  - Should be a **pure function**

* How can you embed two components into one?

```javascript
class MyComponent extends React.Component {
	render() {
		return (
			<div>
				<h1>Hello</h1>
				<Header/>
			</div>
		);
	}
}

class Header extends React.Component {
	render() {
		return <h1>Header Component</h1>
	}
}

ReactDOM.render (
	<MyComponent/>, document.getElementById('content')
);
```

* Explain props in React.
  - Short for properties
  - Are Read-only
  - Are pure i.e. immutable
  - Always **passed down from parent to child component**
  - Used to render dynamic data

```
class MyComponent extends React.Component {
	render() {
		return (
			<div>
				<h1>Hello</h1>
				<Header name="maxx" id="101"/>
			</div>
		);
	}
}

function Header(props) {
	return (
		<div>
			<h1> Welcome : {props.name}</h1>
			<h1> Id is : {props.id}</h1>
		</div>
	);	
}

ReactDOM.render (<MyComponent/>, document.getElementById('content'));
```

* What is a **state** in React and how it is used?
  - Heart of react components
  - Must be kept as simple as possible
  - Determines components rendering and behavior
  - Creates dynamic and interactive components
  - It is accessed via **this.state()**
  - Can update the state using **this.setStat

```
class MyComponent extends React.Component {
	constructor() {
		super();
		this.state = {
			name: 'Maxx',
			id: '101'
		}
	}

	render() {
		return (
			<div>
				<h1>Hello {this.state.name}</h1>
				<h2>Your Id is {this.state.id}</h2>
			</div>
		);
	}
}

ReactDOM.render (
	<MyComponent/>, document.getElementById('content')
);
```

* Diffentiate between **state** and **props**.

| Conditions										| State	| Prop	|
| ---												| :---:	| :---:	|
| 1. Receive initial value from parent Component	| O		| O		|
| 2. Parent Component can change value				| X		| O		|
| 3. Set default values inside Component			| O		| O		|
| 4. Changes inside Component						| O		| X		|
| 5. Set initial value for child Components			| O		| O		|
| 6. Changes inside child Components				| X		| O		|

* How can you update state of a component?
  - Using this.setState() function you can change the state of the component

```
class MyComponent extends React.Component {
	constructor() {
		super();
		this.state = {
			name: 'Maxx', id: '101'
		}
	}

	render() {
		setTimeout( ()=>{this.setState({name: 'Jaeha', id:'222'})}, 2000)
		return (
			<div>
				<h1>Hello {this.state.name}</h1>
				<h2>Your Id is {this.state.id}</h2>
			</div>
		);
	}

}

ReactDOM.render(<MyComponent/>, document.getElementById('content'));
```

* What is **arrow function**? How its used?
  - Also called 'fat arrow function' ( => )
  - Allows to bind the context of components properly since auto-binding is not available by default in ES6
  - Makes easier to work with higher order functions

  - General Way

```
render() {
	return(<MyInput onChange={
		this.handelChange.bind(this) } />)
}
```

  - With Arrow Function

```
render() {
	return(<MyInput onChange={ (e) => this.handleOnChange(e) } />)	
}
```

* Differentiate between **stateful** and **stateless** components.

| Stateful Component																										| Stateless Component																			|
| ---																														| ---																							|
| 1. Stores info components state change in memory																			| 1. Calculates the internal state of the components											|
| 2. Have authority to change state																							| 2. Do not have the authority to change state													|
| 3. Contains the knowledge of past, current and possible future changes in state											| 3. Contains no knowledge of past, current and possible future state changes					|
| 4. Stateless components notifies them about the requirement of the state change, then they send down the props to them	| 4. They receive the props from the Stateful components and treat them as callback functions	|

* What are the different phases of React component's lifecycle?
  - Initial phase
    * getDefaultProps()
    * getInitialState()
    * componentWillMount()
    * render()
    * componentDidMount()

  - Updating phase
    * componentWillReceiveProps()
    * shouldComponentUpdate()
    * componentWillUpdate()
    * render()
    * componentDidUpdate()

  - Unmounting phase
    * componentWillUnmount()

* Explain the lifecycle methods of React components in details.
  - **componentWillMount()** is executed just before rending both on client and server-sice
  - **componentDidMount()** is executed after first render only on the client side
  - **componentWillReceiveProps()** is invoked as soon as the props are received from parent class before another render is called
  - **shouldComponentUpdate()** returns true or false value based on certain conditions. If you want your component to update return **true** else return **false**. By default its false.
  - **componentWillUpdate()** is called just before rendering takes place
  - **componentDidUpdate()** is called just after rendering takes place
  - **componentWillUnmount** is called after the component is unmounted from the dom. It is used to clear up the memory spaces

* What is an **event** in React?
  - **Events** are the triggered reactions to specific actions like mouse hover, mouse click, key press etc
  - React events are similar to HTML, JavaScript events.

* How do you create an event in React?
```
class Display extends React.Component({
	show(evt) {
		// code
	}

	render() {
		// Render the div with an onClick prop (value is a function)
		return <div onClick={this.show}>Click Me!</div>;
	}
});
```

* What are synthetic events in React?
  - Cross browser wrappers around the browsers native event system
  - Combines the browsers behaviors into one API
  - Done to ensure events have consistent properties across different browsers

* What do you understand by refs in React?
  - Refs stands for References
  - Used to return references to a particular element or component returned by render()
  - useful when we need DOM measuremnets or to add methods to the components

* List some of the cases when you should use Refs
  - Managing focus, text selection or media playback
  - Triggering imperative animations
  - Integrating with third-party DOM libraries

* How do you modularize code in React?
  - By using the export and import properties we can write the components separately in different files
```
export default class ChildComponent extends React.Component {
	render() {
		return (
			<div>
				<h1>This is a child component</h1>
			</div>
		)
	}
}
```

```
import ChildComponent from './childcomponent.js';

class ParentComponent extends React.Component {
	render() {
		return (
			<div>
				<App />
			</div>
		)
	}
}

```

* How forms are created in React?
  - HTML form elements maintain their own state in regular DOMs and update themselves based on user inputs
  - In React, state is contained in the state property of the component and is only updated via setState()
  - JavaScript function is used for handling the form submission

* What do you know about controlled and uncontrolled components?
  - Controlled Components
    * Do not maintain their own state
    * Data is controlled by parent component
    * Takes in current values through pros and notifies changes via callbacks

  - Uncontrolled Components
    * Maintain their own state
    * Data is controlled by DOM
    * Refs are used to get their current value

* What are higher order components(HOC)?
  - Custom components which wraps another component
  - They accept dynamically provided child components
  - Do not modify the input component
  - Do not copy any behavior from the input component
  - Are 'Pure' functions
  ![High_Order_Component](https://user-images.githubusercontent.com/32950391/85915069-5b5d8880-b812-11ea-82d3-8ab6b2bf6c39.JPG)

* What can you do with HOC?
  - Code reuse, logic and bootstrap abstraction
  - Render High jacking
  - State abstraction and manipulation
  - Props manipulation

* What are Pure Components?
  - Pure components are the simplest, fastest components which we can write
  - Can replace any component that only has **render()**
  - Enhances the simplicity and performance of the application
```
ReactDOM.render(<h1>Hello</h1>, document.getElementById('content'));
```

* What is the significance of keys in React?
  - Used to identify unique Virtual DOM Elements with their corresponding data driving the UI
  - Helps React to optimize rendering by recycling existing DOM elements
  - Keys must be a unique number or string
  - Instead of re-rendering, with keys React just re-orders the elements
  - Application's performance increases


3) React **Redux**
* What were the major problems with MVC framework?
  - DOM manipulation was very expensive
  - Slow and inefficient
  - Memory wastage
  - Because of circular dependencies, complicated model was created aroound models and views
  ![MVC_Model](https://user-images.githubusercontent.com/32950391/85915299-366a1500-b814-11ea-83b1-548c7cf9fcd1.JPG)

* Explain Flux
  - Architectual patten that enforces uni-directional data flow
  - Controls derived data and enables communication between multiple components
  - Contains a central Store which has authority for all data
  - Any update in data must occur here only
  - Provides stability to the application
  - Reduces run-time errors
  ![Flux](https://user-images.githubusercontent.com/32950391/85915411-49311980-b815-11ea-9959-120276442a04.JPG)

* What is Redux?
  - Redux one of the hottest libraries for front end development
  - Redux is a predictable state container for JavaScript apps
  - Mostly used for applications State Management
  - Applications developed with Redux are easy to test
  - Helps to write applications that behave consistently and can run in different environments

* What are the three principles that Redux follows?
  - Single source of truth
  - State is read-only
  - Changes are made with pure functions

* What do you understand by single source of truth?
  - Redux uses Store for storing all the application state at one place
  - Components state is stored in the Store and they receive updates from the sotre itself
  - The single state tree makes it easier to keep track of changes over time and debug or inspect the application
  ![Single_Source_of_Truth](https://user-images.githubusercontent.com/32950391/85915558-7b8f4680-b816-11ea-8936-022474ebdb38.JPG)

* List down the components of Redux.
  - **Action** - It's an object that describes what happened
  - **Reducer** - It is a place to determine how the state will change
  - **Store** - State/Object tree of the entire application is saved in the store
  - **View** - Simply displays the data provided by the Store

* Show how the data flows through Redux?
  ![Data_Flows_through_Redux](https://user-images.githubusercontent.com/32950391/85915663-6d8df580-b817-11ea-875a-41b7e55f168d.JPG)

* How **Actions** are defined in Redux?
  - Must have **type** property that indicates the type of ACTION being performed
  - They must be defined as String constant
  - You can add more properties to it
  - Actions are created using functions called Action Creators
```
function addTodo(text)
{
	return
	{
		type: ADD_TODO,
		text
	}
}
```

* Explain the role of **Reducer**.
  - Reducers are pure functions which specify how the applications state changes in response to an ACTION
  - Takes in the previous state and an action and returns the new state
  - Determins what sort of update needs to be done based on the type of the action, and returns new values
  - It returns the previous state if no work needs to be done
  ![Role_of_Reducer](https://user-images.githubusercontent.com/32950391/85915806-c6aa5900-b818-11ea-93d4-1b4d4b09331b.JPG)

* What is the significance of Store in Redux?
  - A store is a JavaScript object which can hold the application's state and
  - It provides a few helper methods to access the state, dispatch actions and register listeners
  - With Store the data state can be synchronized from the server level to the client layer without much hassle

```
import { createStore } from 'redux'
import todoApp from './reducers'

let store = createStore(reducer);
```

* How Redux is different from Flux?

| FLUX										| REDUX										|
| ---										| ---										|
| Store contains state and change logic		| Store and change logic are separate		|
| Multiple stores							| Single Store								|
| Flat disconnected stores					| Single store with hierarchical reduces	|
| Single dispatcher							| No dispatcher								|
| React components subscribe to the store	| Container components utilize connect		|
| State is mutable							| State is immutable						|

* What are the advantages of Redux?
  - Predictability
  - Maintainability
  - Server side rendering
  - Developers tool
  - Huge community
  - Ease of testing
  - Precise organization of code


4. React **Router**
* What is React Router?
  - Powerful routing library
  - Helps in adding new screens and flows to the application
  - Keeps the URL in sync with data that's being displayed on the web page
  - Has simple API

* Why switch keyword is used in React Router v4?
  - The 'switch' keyword is used to when you want to display only a single route to be rendered amongst the several defined routes

```
<switch>
	<route exact path='/' component={Home}/>
	<route path='/posts/:id' component={Newpost}/>
	<route path='/posts' component={Post}/>
</switch>
```

* Why do we need a Router in React?
  - Helps in defining multiple routes inside the Router with each leading to a unique **view**
  ![Router_in_React](https://user-images.githubusercontent.com/32950391/85916217-7634fa80-b81c-11ea-9660-694cd134b684.JPG)

* List down the advantages of React Router.
  - API is "All about components"
  - Can be visualized as single root component
  - No need to manually set History value
  - Separate packages for Web and Native platforms
  ![React_Router](https://user-images.githubusercontent.com/32950391/85916255-eb083480-b81c-11ea-81a0-f80b1d2c93f5.JPG)

* How React Router is different from conventional routing?

| Topic				| Conventional Routing														| React Router														|
| :---:				| ---																		| ---																|
| Pages Involved	| Each view corresponds to a new file										| Only single HTML page is involved									|
| URL Changes		| A HTTP request is sent to server and corresponding HTML page is received	| Only the History attribute is changed								|
| Feel				| User actually naviages across different pages for each view				| User is duped thinking he is navigating across different pages	|


# References
---
Edureka! (2017). React Interview Questions and Answers | React Tutorial | React Redux Online Training | Edureka. Retrieved June 26, 2020, from <https://www.youtube.com/watch?v=39ZiaKb1bSA>

---

