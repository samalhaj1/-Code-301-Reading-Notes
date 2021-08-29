![img](https://survivejs.com/aa5a4c6ca72d354fc961ff93a65137b4.png)


**Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?**

render before the componentDidMount 

This is happening because of how React works fundamentally. React is supposed to feel fast, fluent and snappy; 

the application should never get clogged up with http requests or asynchronous code.

The answer is to use the lifecycle methods to control the DOM.

**What is the very first thing to happen in the lifecycle of React?**

componentWillUnmount

**Put the following things in the order that they happen:**

componentDidMount, render, constructor, componentWillUnmount, React Updates

1-componentWillUnmount

2- constructor()

3- render()

4- componentDidMount 

5- React Updates


**What does componentDidMount do?**

It might be helpful to understand some of the React vocabularies a little better.

* When a component is mounted it is being inserted into the DOM. This is when a constructor is called.

* componentWillMount is pretty much synonymous with a constructor and is invoked around the same time.

* componentDidMount will only be called once after the first render.

componentWillMount --> render --> componentDidMount


**1- What types of things can you pass in the props?**

props enable you to pass variables from one to another component down the component tree. 

In the previous example, it was only a string variable. But props can be anything from integers over objects to arrays.

**2- What is the big difference between props and state?**


Image result for What is the big difference between props and state?
Props are immutable, while state is mutable

Although a component is not allowed to change its props, it is responsible for the props of its child components down the component tree.

On the other hand, state is mutable. A stateful component changes its state every time users interact with the app.

**3- When do we re-render our application**


A re-render can only be triggered if a component's state has changed. The state can change from a props change, or from a direct setState change.

The component gets the updated state and React decides if it should re-render the component.

**4- What are some examples of things that we could store in state?**

The data (the value of the counter) is stored within the App component, and can be passed down its children.

## Handling Events

Just like HTML, React can perform actions based on user events.

React has the same events as HTML: click, change, mouseover etc.

**Adding Events**

React events are written in camelCase syntax:

onClick instead of onclick.

React event handlers are written inside curly braces:

onClick={shoot}  instead of onClick="shoot()".

React:

< button onClick={shoot} >Take the Shot!< /button >

HTML:

< button onclick="shoot()" >Take the Shot!< /button >

## Event Handlers

A good practice is to put the event handler as a method in the component class:

**Example:**

Put the shoot function inside the Football component:

       class Football extends React.Component {
        shoot() {
        alert("Great Shot!");
        }
        render() {
        return (
      <button onClick={this.shoot}>Take the shot!</button>
      );
      }
      }

      ReactDOM.render(<Football />, document.getElementById('root'));
      
      
      
 ## What is the react:
 
 ![img](https://survivejs.com/aa5a4c6ca72d354fc961ff93a65137b4.png)
 
 
 React is a JavaScript library that forces you to think in terms of components.
 
 This model of thinking fits user interfaces well. Depending on your background it might feel alien at first.
 
 You will have to think very carefully about the concept of state and where it belongs.

Because state management is a difficult problem, a variety of solutions have appeared. 

In this book, we'll start by managing state ourselves and then push it to a Flux implementation known as Alt. 

There are also implementations available for several other alternatives, such as Redux, MobX, and Cerebral.

**React Renderers**

As mentioned, React's approach decouples it from the web. You can use it to implement interfaces across multiple platforms. 

In this case we'll be using a renderer known as react-dom. It supports both client and server side rendering.























