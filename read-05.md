# Thinking in React

React is, in our opinion, the premier way to build big, fast Web apps with JavaScript. It has scaled very well for Facebook and Instagram.

One of the many great parts of React is how it makes you think about apps as you build them. 
In this document, we’ll walk you through the thought process of building a searchable product data table using React.

## Thinking in React 

### Step 1: Break The UI Into A Component Hierarchy


The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names. If you’re working with a designer, they may have already done this, so go talk to them! Their Photoshop layer names may end up being the names of your React components!

But how do you know what should be its own component? Use the same techniques for deciding if you should create a new function or object. One such technique is the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

Since you’re often displaying a JSON data model to a user, you’ll find that if your model was built correctly, your UI (and therefore your component structure) will map nicely. That’s because UI and data models tend to adhere to the same information architecture. Separate your UI into components, where each component matches one piece of your data model.


* FilterableProductTable (orange): contains the entirety of the example
* SearchBar (blue): receives all user input
* ProductTable (green): displays and filters the data collection based on user input
* ProductCategoryRow (turquoise): displays a heading for each category
* ProductRow (red): displays a row for each product
* If you look at ProductTable, you’ll see that the table header (containing the “Name” and “Price” labels) isn’t its own component. This is a matter of preference, and there’s an argument to be made either way. For this example, we left it as part of ProductTable because it is part of rendering the data collection which is ProductTable’s responsibility. However, if this header grows to be complex (e.g., if we were to add affordances for sorting), it would certainly make sense to make this its own ProductTableHeader component.

Now that we’ve identified the components in our mock, let’s arrange them into a hierarchy. Components that appear within another component in the mock should appear as a child in the hierarchy:

* FilterableProductTable

* SearchBar
* ProductTable

* ProductCategoryRow
* ProductRow


### Step 2: Build A Static Version in React

To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props.

building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing. 

## A Brief Interlude: Props vs State

There are two types of “model” data in React: props and state. 

It’s important to understand the distinction between the two; skim the official React docs if you aren’t sure what the difference is.

### Step 3: Identify The Minimal (but complete) Representation Of UI State


To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state .

The key here is DRY: Don’t Repeat Yourself . Figure out the absolute minimal representation of the state your application needs and compute everything else you need on-demand. For example, if you’re building a TODO list, keep an array of the TODO items around; don’t keep a separate state variable for the count. 
Instead, when you want to render the TODO count, take the length of the TODO items array.


React is all about one-way data flow down the component hierarchy. It may not be immediately clear which component should own what state.


Think of all the pieces of data in our example application. We have:

* The original list of products
* The search text the user has entered
* The value of the checkbox
* The filtered list of products

Let’s go through each one and figure out which one is state. Ask three questions about each piece of data:

1. Is it passed in from a parent via props? If so, it probably isn’t state.

2. Does it remain unchanged over time? If so, it probably isn’t state.

3. Can you compute it based on any other state or props in your component? If so, it isn’t state.


### Step 4: Identify Where Your State Should Live

 Once you've identified data, it should be stated in the application. 
 
 We need to work out which components rely on the state, which can potentially mutate it and which should own it. 
 
 This might not be blatantly obvious when we look at our component hierarchy. 
 
 Remember, React data flow is unidirectional and data flows from the top of a component tree to the bottom. 
 
 There's a three-step process to identifying which component should own state. Firstly, identify every component that render something based on state. 
 
 That means the component receives all, or part of the state as props. 
 
 Then, find a component higher up the tree than all the components that use the state, and put state in this component. 
 
 This could be an immediate owner component or a component even higher up the tree. 
 
 Lastly, if it doesn't make sense for state to live in a common owner component or one doesn't exist, create a new component to hold state, and add it to the hierarchy and appropriate place.


### Step 5: Add Inverse Data Flow

#### What is inverse data flow?
In React, inverse data flow allows us to send data between parent and child components as props, or properties. However, components that are cousins or siblings cannot directly communicate with each other.

Sharing data between parent and child components.

n our Home component, we're defining the handleChange() and handleResponse() functions and then sending them down as props to its child components, CreateAccountForm and AccountSettings. 

The information inputted by the user in these child components is then sent back up to the parent component by invoking those very same functions. 

This allows us to "reuse" these functions without having to copy and paste the same code in both of the child components.


















