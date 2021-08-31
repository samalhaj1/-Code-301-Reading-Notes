## React Forms:

An HTML form is used to collect user input. The user input is most often sent to a server for processing.

The <form> Element
The HTML <form> element is used to create an HTML form for user input:

     <form>
     .
     form elements
     .
     </form>
  
**The < form > element** is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.
  
**The < input > Element**
  
The HTML < input > element is the most used form element.

An < input > element can be displayed in many ways, depending on the type attribute.

Here are some examples:
  
|Type|	Description|
|-----|------------|
|< input type="text" >	|Displays a single-line text input field|
|< input type="radio" >	|Displays a radio button (for selecting one of many choices)|
|< input type="checkbox" >|	Displays a checkbox (for selecting zero or more of many choices)|
|< input type="submit" >	|Displays a submit button (for submitting the form)|
|< input type="button" >	|Displays a clickable button|
  
 ## What are Controlled Components in React?
  
### Controlled Components
  
In React, when handling a form, you’d want a JavaScript function that handles the submission of the form. 
  
The function will have access to the form data entered by the user.
  
This technique is called “controlled components”.
  
  
### How forms are handled in HTML and React?
HTML form elements maintain their own state and update the state based on the user inputs.

In React, it’s a bit different. React keeps a mutable state of components and it gets updated using setState()
  
### How to create a controlled component?
Creating controlled component requires you to combine both HTML and React handling of form elements and making the React state as the controller. So, the same React component that renders the form elements has now more control over those elements and it can control what happens inside those form elements.

A Controlled Component is nothing but a technique of controlling the value of form input elements by Recat.
  
## HTML <textarea> Tag

**Example**
  
A multi-line text input control (text area):

        <label for="review">Review of React Forms:</label>

        <textarea id="review" name="review" rows="4" cols="50">
        Today we will learn about react forms 
        </textarea>
  
**Definition and Usage**
  
The < textarea > tag defines a multi-line text input control.

The < textarea > element is often used in a form, to collect user inputs like comments or reviews.

A text area can hold an unlimited number of characters, and the text renders in a fixed-width font (usually Courier).

The size of a text area is specified by the < cols > and <rows> attributes (or with CSS).

The name attribute is needed to reference the form data after the form is submitted (if you omit the name attribute, no data from the text area will be submitted).

The id attribute is needed to associate the text area with a label.
  
### HTML < select > Tag

**Example**
  
Create a drop-down list with four options:

       <label for="cars">Choose a car:</label>

       <select name="cars" id="cars">
       <option value="volvo">Volvo</option>
       <option value="saab">Saab</option>
       <option value="mercedes">Mercedes</option>
       <option value="audi">Audi</option>
       </select>
  
**Definition and Usage**
  
The < select > element is used to create a drop-down list.

The < select > element is most often used in a form, to collect user input.

The name attribute is needed to reference the form data after the form is submitted (if you omit the name attribute, no data from the drop-down list will be submitted).

The id attribute is needed to associate the drop-down list with a label.

  

  
## Conditional Rendering
  
If you do not want to display the h1 element until the user has done any input, you can add an if statement.

Look at the example below and note the following:

1. We create an empty variable, in this example we call it header.

2. We add an if statement to insert content to the header variable if the user has done any input.

3. We insert the header variable in the output, using curly brackets.
  
### Submitting Forms
You can control the submit action by adding an event handler in the onSubmit attribute:
  
Note that you should use event.preventDefault() to prevent the form from actually being submitted.
  
### Multiple Input Fields
  
You can control the values of more than one input field by adding a name attribute to each element.

When you initialize the state in the constructor, use the field names.

To access the fields in the event handler use the event.target.name and event.target.value syntax.

To update the state in the this.setState method, use square brackets [bracket notation] around the property name.
  
### Value of null for Controlled Input

Specifying the value prop on a controlled component prevents the user from changing the input unless you desire so.

You might have run into a problem where value is specified, but the input can still be changed without consent. In this case, you might have accidentally set value to undefined or null.

The snippet below shows this phenomenon; after a second, the text becomes editable.
                
             ReactDOM.render(<input value="hi" />, mountNode);

            setTimeout(function() {
             ReactDOM.render(<input value={null} />, mountNode);
            }, 1000);






















