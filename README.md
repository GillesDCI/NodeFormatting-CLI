# CLI Text Formatter

A command line tool for formatting and sanitizing strings

## What you will be doing

You will be writing a CLI program that takes a user input as a string. The program will then;

1. Format the string
2. Sanitize the string
3. Return the result

### Example

```bash
$ node index.js "mIAmi   Vice"
Miami Vice
```

## Tasks

### Task 1

Create the files;

- `index.js`
- `formatting.js`
- `messaging.js`

### Task 2

Inside `formatting.js`, create the function `removeWhitespace`

This function should:

1. Take an argument (the string to be formatted)
2. Trim whitespace from the beginning and end of the argument
3. Collapse spaces (ensure only one space appears at a time, no doubles)

##### Example

```shell
> removeWhitespace(" sao tome")
> "sao tome"
> removeWhitespace("kuala lumpur ")
> "kuala lumpur"
```

> Hint: You can use the [trim](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/Trim) method to remove whitespaces

## Task 3

Inside `formatting.js`, create the function `capitalizeInitial`

This function should:

1. Take an argument (the string to be formatted)
2. Make the entire string lowercase
3. Capitalize the first letter

> Hint: You can use the [toLowerCase](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase) method to format a string as lowercase

> Hint: You can use the [toUpperCase](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase) method to format a string as uppercase

##### Example

```shell
> capitalizeInitial("europe")
> "Europe"
> capitalizeInitial("BERLIN")
> "Berlin"
> capitalizeInitial("aSIa")
> "Asia"
```

### Task 4

Inside `messaging.js`, create the function `showHelp`

This function should display in the console, some helpful instructions for the user

##### Example

```bash
$ node index.js "mIAmi   Vice" --help
How to use this program:
    1. When you input a new string with more than 1 space the program will sanitize it.
    2. If you typed the name of a city without capitalization the program will capitalize it.
    3. If you included a Capitalized letter inside the wrong place of your string the program will sanitize it.
Miami Vice
```

### Task 5

Now your functions are created, inside `index.js`;

1. Read the CLI arguments from the user
2. If the string `--help` appears anywhere in the argument list, run the `showHelp` function in `messaging.js`, and terminate the program
3. Otherwise, format and sanitize the string with the functions you created in `formatting.js`, and display the result to the user in the console

## Bonus Tasks

- Your program should be also able to remove symbols, for example all characters that do not match `A-Z`, `a-z` or `0-9`