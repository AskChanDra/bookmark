# JSX

#### What is JSX?

- JSX stands for JavaScript XML.
- JSX allows us to write HTML in React.
- JSX makes it easier to write and add HTML in React.
- JSX converts HTML tags into react elements.
- JSX is an extension of the JavaScript language based on ES6, and is translated into regular JavaScript at runtime.
- Expressions in JSX `{}`
- Inserting a Large Block of HTML
- JSX follows XML rules, and therefore HTML elements must be properly closed.



```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const myelement = React.createElement('h1', {}, 'I do not use JSX!');

ReactDOM.render(myelement, document.getElementById('root'));
```


#### Refrences:

- [React JSX](https://www.w3schools.com/react/react_jsx.asp)
