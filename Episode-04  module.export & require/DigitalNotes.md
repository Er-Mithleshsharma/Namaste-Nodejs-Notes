## Namaste Node.js - Episode 4 Summary 
# Importing and Exporting in Node.js

## Importing and Using

To import a function from a module, use the `require` function. Here's an example:

```javascript
// In file app.js
const greet = require('./greet');
console.log(greet('World')); // Output: Hello, World!
```

## Exporting Multiple Functions/Variables

To export multiple functions or variables, attach them to the `module.exports` object:

```javascript
// In file utils.js
const add = (a, b) => a + b;
const subtract = (a, b) => a - b;

module.exports = { add, subtract };
```

## Importing Multiple Exports

To import multiple exports from a module, use destructuring:

```javascript
// In file app.js
const { add, subtract } = require('./utils');
console.log(add(5, 3));      // Output: 8
console.log(subtract(5, 3)); // Output: 2
```

## How `require` Works

When you use `require` to import a module, Node.js executes the code in the module file. Only the properties of `module.exports` are exposed to the importing file.

Example:

```javascript
// In file data.js
const secret = 'hidden';
const publicData = 'visible';

module.exports = publicData;
```

```javascript
// In file app.js
const data = require('./data');
console.log(data); // Output: visible
console.log(secret); // Error: secret is not defined
```

In the example above, `secret` is not accessible outside `data.js` because it was not exported using `module.exports`.

## .mjs vs. .cjs Modules

### .cjs Modules (CommonJS)

- **File Extension:** `.js` or `.cjs`
- **Module System:** CommonJS
- **Usage:** `require()` and `module.exports`

Example:

```javascript
// In file common.js
module.exports = function() { /* ... */ };
```

### .mjs Modules (ES Modules)

- **File Extension:** `.mjs`
- **Module System:** ES Modules (ESM)
- **Usage:** `import` and `export`

Example:

```javascript
// In file module.mjs
export function greet(name) {
  return `Hello, ${name}!`;
}
```

#### Importing in .mjs

```javascript
// In file app.mjs
import { greet } from './module.mjs';
console.log(greet('World')); // Output: Hello, World!
```

## Differences Between .mjs and .cjs

- **Syntax:** `.cjs` uses `require` and `module.exports`, while `.mjs` uses `import` and `export`.
- **Compatibility:** `.mjs` is the standard ES Module syntax and is compatible with modern JavaScript, while `.cjs` is used for legacy Node.js modules.
- **Use Case:** Use `.mjs` for new projects or when using features of ES Modules, and `.cjs` for legacy code or when using the CommonJS module system.

## Summary

- `module.exports` is used to export functions, objects, or variables from a module.
- `require` imports these exports into another module.
- `.cjs` modules use CommonJS syntax (`require` and `module.exports`), while `.mjs` modules use ES Module syntax (`import` and `export`).
