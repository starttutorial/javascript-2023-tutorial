# Modules

## JavaScript Modules

JavaScript modules allow you to break up your code into separate files. This makes it easier to maintain and manage your code, especially as your application grows. Modules can export functions, objects, or primitive values from one file so they can be reused in other files.

### Using `export` Statements

The `export` statement is used to export functions, objects, or values from a module so they can be used in other modules.

#### Named Exports

Named exports allow you to export multiple values. When using named exports, you must use the same name when importing.

```javascript
// math.js
export function add(a, b) {
    return a + b;
}

export function subtract(a, b) {
    return a - b;
}
```

To use these functions in another module, you need to import them by their exact names:

```javascript
// main.js
import { add, subtract } from './math.js';

console.log(add(5, 3)); // Outputs: 8
console.log(subtract(5, 3)); // Outputs: 2
```

If you want to import multiple named exports, you can do so by listing them within curly braces.

#### Default Exports

A module can also export a single value as the default export, using the `export default` statement. Default exports are useful when you want to export a single entity from a module. 

```javascript
// greet.js
export default function greet(name) {
    return `Hello, ${name}!`;
}
```

When importing a default export, you can name it anything you like because it's the default and there's only one:

```javascript
// main.js
import greet from './greet.js';

console.log(greet('Alice')); // Outputs: Hello, Alice!
```

### Using `import` Statements

The `import` statement is used to bring in the exported values from another module.

#### Importing Named Exports

For named exports, you need to use the exact names of the exported values:

```javascript
// utilities.js
export const pi = 3.14159;
export function circumference(radius) {
    return 2 * pi * radius;
}
```

You import them like this:

```javascript
// main.js
import { pi, circumference } from './utilities.js';

console.log(pi); // Outputs: 3.14159
console.log(circumference(2)); // Outputs: 12.56636
```

#### Importing Default Exports

For default exports, you can name the imported entity whatever you choose:

```javascript
// format.js
export default function formatCurrency(amount) {
    return `$${amount.toFixed(2)}`;
}
```

You import it like this:

```javascript
// main.js
import formatCurrency from './format.js';

console.log(formatCurrency(1234.567)); // Outputs: $1234.57
```

#### Combining Named and Default Imports

You can import both named and default exports from a module in a single statement:

```javascript
// data.js
export const items = ['apple', 'orange', 'banana'];
export default function countItems() {
    return items.length;
}
```

You import them like this:

```javascript
// main.js
import countItems, { items } from './data.js';

console.log(items); // Outputs: ['apple', 'orange', 'banana']
console.log(countItems()); // Outputs: 3
```

### Renaming Imports and Exports

You can also rename imports and exports to avoid conflicts or for clarity:

```javascript
// shapes.js
export function square(x) {
    return x * x;
}

export function circleArea(radius) {
    return Math.PI * radius * radius;
}
```

You can rename them during import like this:

```javascript
// main.js
import { square as sq, circleArea as ca } from './shapes.js';

console.log(sq(4)); // Outputs: 16
console.log(ca(3)); // Outputs: 28.274333882308138
```

### Importing All Exports

If you want to import everything from a module under a single namespace, you can use the `* as` syntax:

```javascript
// constants.js
export const pi = 3.14159;
export const e = 2.71828;
```

You import them like this:

```javascript
// main.js
import * as constants from './constants.js';

console.log(constants.pi); // Outputs: 3.14159
console.log(constants.e); // Outputs: 2.71828
```

### Conclusion

JavaScript modules provide a powerful way to organize and reuse code across different files. By using `import` and `export` statements, you can create modular, maintainable, and scalable applications. Understanding how to use these statements effectively is crucial for modern JavaScript development.
