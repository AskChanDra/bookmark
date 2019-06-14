# React JS

- A JavaScript library for building user interfaces.
- Is used to build SPAs.
- A tool for building UI components.

##### How does it work?
- React creates a VIRTUAL DOM in memory.
- React only changes what needs to be changed!

#### Example
```html
<!DOCTYPE html>
<html>
  <script src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>
  <script src="https://unpkg.com/babel-standalone@6.15.0/babel.min.js"></script>
  <body>
  
    <div id="mydiv"></div>

    <script type="text/babel">
      class Hello extends React.Component {
        render() {
          return <h1>Hello World!</h1>
        }
      }
    </script>

  </body>
</html>
```

#### Create React App

1 Install NPM Package
```bash
npm install -g create-react-app
```

2 Create new React App `myapp`
```bash
npx create-react-app myapp
```

3 Run the React App
```bash
cd myapp
npm start
```

4. Open `localhost:3000`

