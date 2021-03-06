# Morning challenge: Convert ES6 code to ES5

## Setup

1. Clone this repository to your computer.

2. Run `node assertEquals.js` from the repository directory to run the tests in Node.

## Description

The code in `assertEquals.js` is written using ES6 syntax. Try to convert as much of it as possible to ES5.

## Learning outcomes

- Recognising some common ES6 features and understanding how they relate to familiar ES5 features.
- Making non-breaking changes in an unfamiliar codebase without getting lost in the overall structure.

## Instructions

Don't worry – you don't need to know any ES6 already. Everything required is referenced with comments in the code.

- Before you change anything, run the code in Node to see the output. None of the changes you make should affect the output.

- You probably won't have time to change all of the ES6 syntax in an hour 

- Pick a few features that you're interested in, read some documentation, try to replace them with ES5, then run the file again in Node to check that the output hasn't changed. 

- The first time each ES6 feature appears in the code, you'll find a comment on the previous line telling you what features to look for, which you can look up in the list below to find a quick fix.

- The code makes use of several ES6 features:

    - If you're not feeling hugely comfortable with ES6, then focus on understanding and replacing some of the features near the top of the following list. 

    - If you already feel comfortable with ES6, feel free to skip ahead to some of the features at the end of the list – the two at the bottom are particularly challenging.

The features (ordered by how difficult it will be to replace them with ES5, from easiest to hardest) are:
---
- [block-scoped variables](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/let): Declared with `let`. Similar to `var`s, but scoped to a single block (essentially the set of curly brackets it's declared in). **Quick fix**: Replace with a `var` and test that your code hasn't broken.

- [constants](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/const):  Declared with `const`. Similar to a `let`, but the reference can't be changed after it's been declared. **Quick fix**: Replace with a `var` and test that your code hasn't broken.

- [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions): Similar to an ES5 function, but uses a 'fat arrow' (`=>`) between the parameters and the function body. **Quick fix**: Replace with a `function` and test that your code hasn't broken.

- [template literals](http://es6-features.org/#StringInterpolation): Similar to a string, but uses backticks (`` ` ``) instead of quotes (`'`) and allows you to insert expressions into the string using the syntax `${expression}`. **Quick fix**: Concatenate multiple strings and expressions together instead using the `+` symbol.

- [default parameter values](http://es6-features.org/#DefaultParameterValues): Allows you to assign a default value to a parameter in a function if no argument is given. **Quick fix**: Check if the parameter ```=== undefined``` in the function body and assign a default value within the if statement.

- [the spread operator](http://es6-features.org/#SpreadOperator): Separates an array out into its elements so they can be added to a new array or used as parameters in a function. **Quick fix**: (when creating a new array) use `array1.concat(array2)` to add all items from the second array to the first.

- [object destructuring](http://es6-features.org/#ParameterContextMatching): Assigns multiple keys from an object to separate variables or parameters at the same time. **Quick fix**: Manually assign each key to a new variable.

- [the Set data structure](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Set): A new type of object – similar to an `Array`, but each unique element can only appear once. Created using `new Set(iterable)`. **Quick fix**: (when used to create a unique set from an array with repeating elements) create a new array with repeating elements filtered out. Google will help.

- [class definitions](http://es6-features.org/#ClassDefinition): Allows you to define classes using `class`, for class-based object oriented programming. **Quick fix**: Replace class with a traditional constructor function and prototype methods.


## Bonus

If you managed to replace all of the features, congratulations! You should now be able to run the code in any web browser and see the same results that you'd get in Node. Give yourself a pat on the back for your services to accessibility.

Did you replace the `const`s and `let`s with `var`s? Can you think of any situations where that wouldn't work? What could you do differently to mimic that functionality? How about arrow functions and sets?

If you have time remaining, read up on a piece of software called [Babel](https://babeljs.io/) – you'll be hearing a lot more about it in future.
