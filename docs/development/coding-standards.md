# Coding Standards
When contributing to GesEnterprise please follow the standards below.  
Based on [Marlin Coding Standards](https://marlinfw.org/docs/development/coding_standards.html)

## Coding Style
### Indentation
* Use 2 spaces* and don't use tabs for indentation. _Set your editor to use 2 spaces!!_
    * For VS Code it can be changed on the bottom right corner

<sup>* Except for documentation since MKDocs requires 4 spaces for lists</sup>
```js
if (user.type = "employee") {
  console.log("User is employee");
}
```

### Brace-style
If vertical spacing makes code more readable, add one extra blank line rather than using a different brace style.

* Known by the Ancients as ["One True Brace Style"](https://en.wikipedia.org/wiki/Indentation_style#Variant:_1TBS_.28OTBS.29)
* Place opening braces at the end of the line: `if (a == 1) {`
* Do the same for a declaration line: `function pizza(slices) {`
* Vertically align closing braces to the opening line.  
#### Example:
```js
function pizza(slices) {
  if (slices > 2) {
    ...
  } else {
    ...
  } 

  switch (slices) {
    // For small amounts of code make it into a one-liner
    case 1: console.log("1 Slice"); break;
    case 2: console.log("2 Slices"); break;
    case 3: console.log("3 Slices"); break;
    // For big-ish amounts of code use the following style of a case
    case 4:
      console.log("4 Slices");
      ...
      break;
    case default: console.log("No good slices"); break;
  }
}
```
### Whitespace and semicolons
Unlike in C, whitespace in JavaScript source can directly impact semantics. Semicolons end statements in JavaScript. Because of automatic semicolon insertion (ASI), some statements that are well formed when a newline is parsed will be considered complete, as if a semicolon were inserted just prior to the newline. Therefore, to avoid any weird cases, semicolons are mandatory.
```js
let semi = "Semicolon please";
```

### Spacing
* One space after control keywords:  
`if (…)`, `while (…)`, `do {…} while(…)`, `switch (…)` etc.
* No space between a function and its arguments: ` let val = pizza(…)`;
* Use one space around (on each side of) for variables:  
`let myVar = aVar + bVar * cVar;`  
`const myVal = (a * b + b * c);`

### Commenting
Comments are good, but avoid over-commenting. Never try to explain how your code works in a comment: it’s much better to write the code so that the working is obvious, and it’s a waste of time to explain badly written code.

Generally, you want your comments to explain what your code does, not how. Keep comments inside a function body short. If a function is so complex that you need to separately comment parts of it, consider splitting it up into simpler units. Make small comments to note or warn about something particularly clever (or ugly), but avoid excess. Reserve detailed comments for the head of the function, explaining what it does, and possibly why it does it.

Use JSDoc-style comments for functions, classes, and other defined entities.
```js
/**
 * Represents a book.
 * @function
 * @param {string} title - The title of the book.
 * @param {string} author - The author of the book.
 */
function book(title, author) {
  ...
}
``` 

Use the single-line style comments with `//` for comments under 3 lines.
```js
// A short comment should only
// take a maximum of 3 lines.
// Else use a multi-line comment
```

For comments over 3 lines use the multi-line/comment block.
```
/*
The following does not work due to the fact
that the pizzas are too old to be good enough.
Therefore support has been dropped for pizzas,
this come remains for legacy purposes.
Also, say hello to multi-line comments.
*/
```

### Variables
#### Naming
* Use simple names for variables
* Use Camel Case when naming variables:  
`const camelCase = "hi";`  
`let pizzaSlices = 2;`

#### Types
* Variables should not be `var` or no identifier (as this will make it global).
* Use `let` and  `const` for variables