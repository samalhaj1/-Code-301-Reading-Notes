# Understanding the JavaScript Call Stack
![ ](https://www.javascripttutorial.net/wp-content/uploads/2019/12/JavaScript-Call-Stack.png )

## 1. What is a ‘call’?

The call stack is used by JavaScript to keep track of multiple function calls. 

It is like a real stack in data structures where data can be pushed and popped and follows the Last In First Out (LIFO) principle. 

We use call stack for memorizing which function is running right now. The below example demonstrates the call stack.

* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
* Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

## 2. How many ‘calls’ can happen at once?

many times

## 3. What does LIFO mean?
A stack data structure follows the same principle and it's called a LIFO data structure. LIFO means last in first out, 

the same way as a stack of dinner plates or other types of the stack in the real world works—the most recent element added to the stack should be the first out.

## 4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

![ ](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/Call_stack_layout.svg/342px-Call_stack_layout.svg.png )
## 5. What causes a Stack Overflow?
A stack overflow is an undesirable condition in which a particular computer program tries to use more memory space than the call stack has available. 

In programming, the call stack is a buffer that stores requests that need to be handled.

The most-common cause of stack overflow is excessively deep or infinite recursion, 

in which a function calls itself so many times that the space needed to store the variables and information associated with each call is more than can fit on the stack.


# JavaScript error messages


## 1. What is a ‘refrence error’?
An #REF error (the “ref” stands for reference) is the message Excel displays when a formula references a cell that no longer exists, usually caused by deleting cells that a formula is referring to.

## 2. What is a ‘syntax error’?
An exception caused by the incorrect use of a pre-defined syntax. Syntax errors are detected while compiling or parsing source code. 

For example, if you leave off a closing brace ( } ) when defining a JavaScript function, you trigger a syntax error.

## 3. What is a ‘range error’?
Description. A RangeError is thrown when trying to pass a value as an argument to a function that does not allow a range that includes the value. 

This can be encountered when: passing a value that is not one of the allowed string values to String.

## 4. What is a ‘tyep error’?

The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type.

**A TypeError may be thrown when:**

* an operand or argument passed to a function is incompatible with the type expected by that operator or function; or
* when attempting to modify a value that cannot be changed; or
* when attempting to use a value in an inappropriate way.


## 5. What is a breakpoint?

A breakpoint is a point in the program where the code will stop executing. 

For example, if the programmer amended the logic error in the trace table example they may wish to trigger a break point at line 5 in the algorithm.

## 6. What does the word ‘debugger’ do in your code?

A debugger is a tool that is typically used to allow the user to view the execution state and data of another application as it is running. 

Debuggers allow users to halt the execution of the program, examine the values of variables, step execution of the program line by line, and set breakpoints on lines or specific functions that, when hit, will halt execution of the program at that spot. In this view, seeing how the program is viewed by their computer, the user can discover how a program flows, identify incorrect code and data, and find semantic errors in the program.
















