# Learn to Code: ES6
Galvanize JavaScript ecmascript 6 class

Brought to you by Galvanize. Learn more about the way we teach code at [galvanize.com](http://galvanize.com).

Get to this repo by typing in URL: **www.github.com/GTLook/ES6**

## Overview
The goal of this brief course is to provide you with a fun introduction to the advantages of using EMCAScript 6.

#### Here's what we'll be doing:
* Overview of basic EMCAscript6 changes and JavaScript concepts
* Changing a simple function using ES6 javascript
* Playing around and break things


## Setting up your computer


#### Please set up the following:

* A web browser to see what we're working on as others see it (Recommend Google Chrome: [chrome.google.com] (http://chrome.google.com))
* We will be using an online text editor for this workshop. You can sign up here: [https://repl.it/](https://repl.it/) 


## What this workshop is

A super friendly introduction to ES6 JavaScript! 

You can't learn EVERYTHING in ~2 hours. But you can learn enough to get excited and comfortable to keep working and learning on your own! Come to our almost weekly code hours [meetups](https://www.meetup.com/Learn-Code-Seattle/events/) to ask questions if you get stuck and show off what you've been working on!

- This course is for beginners
- Ask Questions!
- Answer Questions!
- Help others when you can
- Its ok to get stuck, just ask for help!
- Feel free to move ahead
- Be patient and nice


## About me:

Hello I'm [Gavin Look](https://www.linkedin.com/in/gavinlook/). I'm a fullstack web developer that graduated from the Galvanize web developer program.  I love writing concise and robust code using ES6 and am currently working on AR projects that enhance user experince!

- gitHub: [GTLook](https://github.com/GTLook/)
- LinkedIn: [GavinLook](https://www.linkedin.com/in/gavinlook/) 
- Email: [GTLook@gmail.com](mailto:GTLook@gmail.com)


## Further Introductions! About you!

Give a quick Intro!

- Whats your name?
- Whats your background?
- Why are you interested in JavaScript?

## What is javaScript?

### A very brief history

Created by Brendan Eich in 1995 in ONLY 10 days during his time at Netscape Communications.

A lot of updates have happened of course since then, but its still fun to see some of the [quirks](https://www.destroyallsoftware.com/talks/wat) still in the language!

Read more about the history of JavaScript [here](https://en.wikipedia.org/wiki/JavaScript).

Javascript is often used with HTML and CSS to create dynamic web pages. 

### What is EMCAScript 6?

ECMAScript 6 is also known as ES6 and ECMAScript 2015

Some people like to call it JavaScript 6.

This chapter will introduce some of the new features in ES6.


### What can you do with ES6 JavaScript

- JavaScript let
- JavaScript const
- JavaScript default parameter values
- Array.find()
- Arrow Functions
- Destucturing!
- template literals
- [And so much more](https://es6-features.org/)


## ES6 JavaScript Basics:

### Variable Scope:
We're going to start with the basics var vs let and const.  

Feel free to try these code samples out in your developer console(I'll show you how) or your repl!

#### Let:

The let statement allows you to declare a variable with block scope.

```
var x = 10;
// Here x is 10
{ 
    let x = 2;
    // Here x is 2
}
// Here x is 10
```

#### Const:

The const statement allows you to declare a constant (a JavaScript variable with a constant value).

Constants are similar to let variables, except that the value cannot be changed.

```
var x = 10;
// Here x is 10
{ 
    const x = 2;
    // Here x is 2
    x = 3 //this will return an error!
}
// Here x is 10
```


#### Default Parameter Values:

ES6 allows function parameters to have default values.  These values are passed into a fucntion when no other value is given.

```
function myFunction(x = 10, y = 10) {
    // y is 10 if not passed or undefined
    return x + y;
}
myFunction(1,2) // will return 3
myFunction(5); // will return 15
myFunction(); // will return 20
```


## Arrow Functions

Arrow functions allows a short syntax for writing function expressions.

You don't need the function keyword, the return keyword, and the curly brackets.

Arrow functions do not have their own this. They are not well suited for defining object methods.

Arrow functions are not hoisted. They must be defined before they are used.

Using const is safer than using var, because a function expression is always constant value.

You can only omit the return keyword and the curly brackets if the function is a single statement. Because of this, it might be a good habit to always keep them:

```
// ES5
function mult(x, y) {
     return x * y;
}

//or

var mult = function(x, y) {
     return x * y;
}

// ES6
const mult = (x, y) => x * y;

// In all cases
mult(2, 5) // Will return 10
```

Try it out! 


## Array.find():
The find() method is a new ES6 method that returns the value of the first array element that passes a test function.

This example finds (returns the value of ) the first element that is larger than 18:

```
var numbers = [4, 9, 16, 25, 29];
var first = numbers.find(myFunction);

function myFunction(value, index, array) {
    return value > 18;
}
```


## Comparison Operators:
Comparison Operators are used quite frequently in programming. Its a great way to compare and use data.

Again we won't cover ALL of the comparison operators in this workshop, but you can see a full list of them [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

- `==` Equal
- `===` Strict Equal
- `!=` Not Equal
- `>` Greater Than
- `>=` Greater Than or Equal
- `<` Less Than
- `<=` Less Than or Equal

Example:

`current_score >= highest_score`
This would return a boolean value. Depending on the values of these variables this would return either `true` or `false`. Try it in your console using numbers instead of variables!


## Functions
Reduce, Reuse, Recycle

Functions make it easy to reuse code. If you find yourself repeating code you may want to turn it into a function!

Example:
This function takes in two arguments(a, b) and returns the value of them added together. 

```
function add(a, b) {
	return a + b; 
};
```
to use the function call it by writing its name and open/close parenthesis(). With arguments passed inside the parenthesis():

- `add(5,5)` | output: 10
- `add(2,5)` | output: 7

In this simple example you're not saving a ton of code, but imagine a function that uses many lines of code! 


## Conditionals

When writing a program you'll often want to check if data meets a certain condition or not. We can use conditionals to make decision about our data and create different outcomes

 In javascript you'll often use the `if` statement. This may be followed by `else if` or `else` depending on how many conditions need to be checked.

Example:

```
if (guess == answer) {
    message = "You Win!";
} else if (guess < answer) {
    message = "Your guess is too low!";
} else if (guess > answer){
    message = "your guess is too high!";
} else {
	message = "I think you entered something wrong...";
}
```

## Loops
We're going to go over some of the basic loops in javascript, but yet again we're not going to cover everything, so you may want to read more about loops [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration).

Loops are used when you want to repeat something. You can repeat the exact same thing, or change some variable and repeat the action again.

two common types of loops are `for` and `while`.
`for` loops are often used to run a loop a specified amount of time.

`while` loops are often used to run a loop indefinitely until certain criteria are met.

Example:

This `for` loop will run 5 times, and print out the value of `i` to the console. 

```
var i;
for (i = 1; i <= 5; i++) {
    console.log(i)
}
```

If `i` were set to 1 it would run this loop and print the string until the value of `i` changed. If you run this in your browser it will probably crash it!

```
var i = 0;
while (i == 1) {
    console.log("I will crash your browser")
}
```


## Interact with dialog boxes
using dialog boxes can be simple way to get started interacting with users.

Alert: Pop up information in a dialog box

`alert("Hello, I'm a pop up");`
 
Prompt: get information from a user in dialog box

`prompt("I'm a pop up you can type in!")`


## Lets do some code!
You just learned a lot! Lets put it together and build something!

Sign up if you haven't already and create a new project: https://repl.it/


We're going to build a number guessing game using:

- variables
- Comparison Operators
- Conditionals
- loops
- functions
- dialog boxes

If you get stuck or want to look ahead at the completed project you can view it [here](https://repl.it/@SageElliott/GuessingGame).

What are some ideas for improvements? 

- Exit on command
- data validation
- input the number range from popup
- output grammar depending on number of tries


# YOU DID IT! YOU'RE NOW A PROGRAMMER!

### Welcome! :)

### Keep learning!



## What is Galvanize?
###### We are a community!


## Relevant Upcoming Events at Galvanize
 
We host sooo many events! check out out [calendar](https://www.galvanize.com/seattle/events)

- [Learn to Code Workshop: Intro to Machine Learning](https://www.meetup.com/Seattle-Data-Science/events/255034878/) - Every Thursday 6:30 PM to 8:30 PM

- [Practicing Coding Interviews](https://www.meetup.com/PSPPython/events/shfwgqyxnblb/) - Monday, October 8, 2018
6:30 PM to 8:30 PM

- [PuPPy Programming Night](https://www.meetup.com/PSPPython/events/zdzrxpyxnbpb/) - Every Thursday 6:30 PM to 8:45 PM

- More Learn to codes coming soon!!!

A weekly list of meetups I think I awesome in Seattle [here](http://sageelliott.com/meetups/).


#### Part-Time Courses
- [Data Science Fundamentals](https://www.eventbrite.com/e/data-science-fundamentals-intro-to-python-seattle-108-1114-tickets-47489110207) - 10/8/2018
- [Data Analytics](https://www.galvanize.com/seattle/data-analytics) - 10/23/2018
- [Structured Study Program at Hack Reactor](https://getcoding.hackreactor.com/ssp-overview/) - 11/5/2018 or 11/12/2018  ***If you're ineterested in learning more about web development THIS IS A GREAT OPTION!!!!! 


#### Immersive Bootcamp
- [Data Science](https://www.galvanize.com/seattle/data-science) - 1/22/2019
- [Software Engineer](https://www.galvanize.com/seattle/web-development) - 1/7/2019


#### Co-working Space
[work in our building!](https://www.galvanize.com/entrepreneur)


## Questions:
Please feel free to reach out to Sage Elliott with any questions!

- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)

#### About the Instructors

[Sage Elliott](https://www.linkedin.com/in/sageelliott/) is a technology evangelist for Galvanize based in Seattle. Previously he worked as a Software and hardware engineer for startup around Seattle WA and Melbourne Fl.

You can email him at [sage.elliott@galvanize.com](mailto:age.elliott@galvanize.com) or tweet [@sagecodes](https://twitter.com/sagecodes) for any further questions.



