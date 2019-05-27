# Parcel JS

- Blazing fast, zero configuration web application bundler
- Parcel has out of the box support for JS, CSS, HTML, file assets, and more - no plugins needed.
- Code is automatically transformed using Babel, PostCSS, and PostHTML when needed - even `node_modules`.
- Using the dynamic `import()` syntax, Parcel splits your output bundles so you only load what is needed on initial load.
- Parcel automatically updates modules in the browser as you make changes during development, no configuration needed.
- Parcel prints syntax highlighted code frames when it encounters errors to help you pinpoint the problem.
  
##### index.html

```html
<html>
<body>
  <script src="./index.js"></script>
</body>
</html>
```
1. Install with yarn:

```bash
yarn global add parcel-bundler
```

or with npm:

```bash
npm install -g parcel-bundler
```

2. Parcel can take any type of file as an entry point, but a HTML or JavaScript file is a good place to start. If you link your main JavaScript file in the HTML using a relative path, Parcel will also process it for you, and replace the reference with a URL to the output file.

##### index.js

```js
// import another component
import main from './main';

main();
```

##### main.js

```js
// import a CSS module
import classes from './main.css';

export default () => {
  console.log(classes.main);
};
```

#### main.css

```css
.main {
  /* Reference an image file */
  background: url('./images/background.png');
  color: red;
}
```

3. Parcel has a development server built in which will automatically rebuild your app as you change files and supports hot module replacement for fast development. Just point it at your entry file:

```bash
parcel index.html
```
to start a dev server. Importing JavaScript, CSS, images, and more just works!

Now open `http://localhost:1234/` in your browser. If needed, you can also override the default port with the `-p` option. Add `--open` to automatically open a browser.

```bash
parcel index.html -p 3000 --open
```

#### Refrences:

- [A curated list of awesome Parcel resources, libraries, tools and boilerplates](https://github.com/parcel-bundler/awesome-parcel)
