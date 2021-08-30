## react

![react]( https://tsc-website-production.s3.amazonaws.com/uploads/2018/05/React-Native.png)



**1- What does .map() return?**

The map() method calls the provided function once for each element in an array, in order.

**2- If I want to loop through an array and display each value in JSX, how do I do that in React?**

using forEach

**3- Each list item needs a unique ____.**

key

**4- What is the purpose of a key?**

React's key prop gives you the ability to control component instances. 

Each time React renders your components, it's calling your functions to retrieve the new React elements that it uses to update the DOM.

**1- What is the spread operator?**

The Spread operator lets you expand an iterable like an object, string, or array into its elements while the Rest operator does the inverse by reducing a set of elements into one array.

**2- List 4 things that the spread operator can do.**

1. Passing props
2. Generating multiple component instances with common props
3. Setting the state with dynamic key name
4. Adding a single item to the start or the end of an array
 

**3- Give an example of using the spread operator to combine two arrays.**

    let fruits = ["apples", "bananas"];
    let vegetables = ["corn", "carrots"];
    let produce = [...fruits, ...vegetables];
    //["apples","bananas","corn","carrots"]

**4- Give an example of using the spread operator to add a new item to an array.**

    let arr1 = ['A', 'B', 'C'];

    let arr2 = ['X', 'Y', 'Z'];

    let result = [...arr1, ...arr2];

    console.log(result); // ['A', 'B', 'C', 'X', 'Y', 'Z']
    // spread elements of the array instead of taking the array as a whole

**5- Give an example of using the spread operator to combine two objects into one.**

    const a = ['to', 'code'];
    const b = ['learning', ...a, 'is', 'fun']; 
    console.log(b); //> ['learning', 'to', 'code', 'is', 'fun']

**1- In the video, what is the first step that the developer does to pass functions between components?**

using props

**2- In your own words, what does the increment function do?**

determines the next node at the same level

**3- How can you pass a method from a parent component into a child component?**

1. Create a child component and put the below code inside that component.

          import React from "react";
          export default function Child({data, onChildClick}) {
          return (
          <div className="child">
          <button onClick={onChildClick}>{data}</button>
         </div>
         );
         }
     
here we have created a child function and inside that, we are creating a simple button whose text data and onclick event will be coming from the parent component.

we have passed data and onChildClick props as an object argument to the child function.

2. Now we will import the child component to our parent component.


            import Child from './Child'
      
      
3. Then inside your parent function create another function to run our desire event and pass the child component to return.


         import React from "react";
         import "./styles.css";
         import Child from './Child'
         export default function Parent() {
         function clickAlert(){
         alert("I am working")
         }
         return (
         <div className="App">
         <Child data="Click here" onChildClick={clickAlert} />
         </div>
         );
         }

**4- How does the child component invoke a method that was passed to it from a parent component?**

Create a boolean variable in the state in the parent class. Update this when you want to call a function. 

Create a prop variable and assign the boolean variable. 

From the child component access that variable using props and execute the method you want by having an if condition.


## Lists and Keys

### Rendering Multiple Components

* Map() takes a list and returns a transformed new list


* Escape the JavaScript within JSX using {}

## Basic List Component

* Usually you would render lists inside a component.

* We can refactor the previous example into a component that accepts an array of numbers and outputs a list of elements.

      function NumberList(props) {
      const numbers = props.numbers;
      const listItems = numbers.map((number) =>
      <li>{number}</li>
      );
      return (
      <ul>{listItems}</ul>
      );
      }

      const numbers = [1, 2, 3, 4, 5];
      ReactDOM.render(
       <NumberList numbers={numbers} />,
       document.getElementById('root')
       );
    
When you run this code, you’ll be given a warning that a key should be provided for list items. 

A “key” is a special string attribute you need to include when creating lists of elements. We’ll discuss why it’s important in the next section.


### Definition and Usage

* The keys() method returns an Array Iterator object with the keys of an array.

* keys() does not change the original array.

**Syntax**

* array.keys()

**Parameter Values**

* No parameters.


### Component Keys Explained

* Keys identify which components have changed, are added, or removed

* Arrays of Components should have unique keys

* Database IDs can make good Keys

* Indexes of the Components are a good backup

* Keys live on the components

* Keys do not live on the content of the component



       ListItem = (props) => {
       // Correct! There is no need to specify the key here:
       return <li>{props.value}</li>;
       }

       NumberList = (props) => {
       const numbers = props.numbers;
       const listItems = numbers.map((number) =>
       // Correct! Key should be specified inside the array.
       <ListItem key={number.toString()}
              value={number} />

       );
       return (
      <ul>
      {listItems}
       </ul>
      );
      }

       const numbers = [1, 2, 3, 4, 5];

       ReactDOM.render(
       <NumberList numbers={numbers} />,
       document.getElementById('root')
       );
       
       
       

















