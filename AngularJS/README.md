# Angular JS

- Angular is a full featured JavaScript Framework created & maintained by Google and is used for building front-end applications or the front-end part of a full stack application.

- Angular is very popular in large enterprise.

##### Why use Angular?

- Organized front-end structure ( Components, Modules, Services )
- Extremley powerfull & full featured
- All in one solution ( Routing, HTTP, RxJS, etc)
- Build powerful SPA apps
- MVC - Model, View, Controller design pattern
- TypeScript
- Fantastic CLI

#### Learn Before Learning Angular

- JavaScript Fundamentals (Objects, Arrays, Conditionals, etc)

##### It may help to learn theme first:

- TypeScript
- Classes
- High Order Array Methods - forEach, map, filter
- Arrow Functions
- Promises & Observables
- MVC Pattern

#### Angular Way

- Uses TypeScript for static types ( variables, functions, params )
- Component based (Like other frameworks )
- Uses "services" to share data/functionality between components
- Concept of "modules" ( root module, forms module, http module, etc)
- Uses RxJS "Observables" for async operations
- Steep Learning curve relative to other frameworks

#### Angular CLI

- Powerful tool for generating apps, modules, components, services etc

```bash
ng new myapp
ng serve
ng build
```

```bash
ng generate component todos
ng generate service todo
ng generate module app-routing
```
#### Todo App : The anatomy of a Component

```javascript
import { Component, Onlnit }  from '@angular/core';

@Component({
 selector: 'app-root',
 templateUrl: './app.component.html',
 styleUrls: [.....to be continue...........
 ```
 
 
 References:
 
 - Angualr Crash Course 2019 ( Traversy Media) : https://youtu.be/Fdf5aTYRW0E?t=613
