#### What is ES6?

- ES6 stands for ECMAScript 6.
- ECMAScript was created to standardize JavaScript, and ES6 is the 6th version of ECMAScript, it was published in 2015, and is also known as ECMAScript 2015.

#### Why Should I Learn ES6?

-React uses ES6, and you should be familiar with some of the new features like:
- Classes
- Arrow Functions
- Variables (let, const, var)

#### Classes

```js
class Car {  constructor(name) {
    this.brand = name;
  }

  present() {
    return 'I have a ' + this.brand;
  }
}

class Model extends Car {
  constructor(name, mod) {
    super(name);
    this.model = mod;
  }  
  show() {
      return this.present() + ', it is a ' + this.model
  }
}
mycar = new Model("Ford", "Mustang");
mycar.show();
```

#### Arrow Functions
-  shorter function syntax
- Before
```js
hello = function() {
  return "Hello World!";
}
```

- After
```js
//With Arrow Function
hello = () => {
  return "Hello World!";
}

// Return value by default
hello = () => "Hello World!";

// With Parameter
hello = (val) => "Hello " + val;

// without parentheses
hello = val => "Hello " + val;
```

#### What About this?
- The handling of this is also different in arrow functions compared to regular functions.
- In short, with arrow functions there are no binding of `this`.
- In regular functions the `this` keyword represented the object that called the function, which could be the window, the document, a button or whatever.
- With arrow functions the `this` keyword always represents the object that defined the arrow function.

##### Usual function
```js
class Header {
  constructor() {
    this.color = "Red";
  }

//Regular function:
  changeColor = function() {
    document.getElementById("demo").innerHTML += this;
  }
}

myheader = new Header();

//The window object calls the function:
window.addEventListener("load", myheader.changeColor);

//A button object calls the function:
document.getElementById("btn").addEventListener("click", myheader.changeColor);
```

Output : [object Window][object HTMLButtonElement]

##### Arrow Function

```js
class Header {
  constructor() {
    this.color = "Red";
  }

//Arrow function:
  changeColor = () => {
    document.getElementById("demo").innerHTML += this;
  }
}

myheader = new Header();


//The window object calls the function:
window.addEventListener("load", myheader.changeColor);

//A button object calls the function:
document.getElementById("btn").addEventListener("click", myheader.changeColor);
```

- Output : [object Object][object Object]

#### Variables

- `var` : var has a function scope, not a block scope.

- outside of a function, it belongs to the global scope.
- inside of a function, it belongs to that function.
- inside of a block, i.e. a for loop, the variable is still available outside of that block.

- `let` : let has a block scope.

- let inside of a block, i.e. a for loop, the variable is only available inside of that loop.

- `const` : const has a block scope.

- const is a variable that once it has been created, its value can never change.



















