> [home](../../home.md)
# Javascript Functions

## What is a Function

set of instructions

## How to declare

### Defining/declaring Function

    function sayHello () {
    console.log("Hello!")
    }

### Calling/executing Function

    sayHello()

## Argument

> An Argument is the section in parenthesis here: `function sayHello (name)`. It is a keyword used to reference what is entered when the **_function_** is **_called_**, for example: `sayHello("Tim")`.

> When using multiple arguments `function sayHelloAndAge(name, age)`.

> It is important to use the same order of Arguments when **_Calling_** a function.

**_To print `"Tim"`:_**

    function sayHello (name) {
        console.log(name)
        }
    sayHello("Tim")

**_`To print "Hello Tim"`:_**

    function sayHello(name) {
      console.log('Hello ' + name)
    }

    sayHello('Tim')

**_To print `"Hello Tim You are: 33 years old"`:_**

    function sayHelloAndAge(name, age) {
      console.log('Hello ' + name)
      console.log('You are: ' + age + ' years old')
    }

    sayHelloAndAge('Tim', '33')

## Returning a Function

> Ends execution of the function and outputs a value, which can be accessed with a **_function caller_**.

**_To return add argument 1 and argument 2 (1+1=3):_**

    function addTogether(num1, num2) {
      return num1 + num2
    }

    let newNumber = addTogether(1, 2)
    //function caller

    console.log(newNumber)
    //to print

> `console.log(addTogether(1,2))` also works.

### Activities of note:

> Return the string 'Hello world!' from the function named `hello`.

    function hello() {
      return 'Hello world!'
    }

> Write a function named `warn` that takes a parameter (it will be a string) and returns the string parameter duplicated, with a space between each string.  
> In addition, the value that will be returned should be logged to the console before being returned.

    function warn(para) {
      console.log(para + ' ' + para)
      return para + ' ' + para
    }
    let warnIs = warn('Fire')
