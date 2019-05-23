# SASS

##### Install

- NodeJS : npm

```bash
npm install -g sass
```

- Windows

```bash
choco install sass
```

- Mac OS

```bash
brew install sass/sass/sass
```

##### SCSS to CSS

```bash
sass source/stylesheets/index.scss build/stylesheets/index.css
```

##### VSCode extension
-   [Live SASS Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)


##### Variables

- SCSS

```scss
$font-stack : Helvetica, sans-serif;
$primary-color : #444;

body {
  font : 100% $font-stack;
  color : $primary-color;
}
```
- CSS
```css
body{
  font: 100% Helvetica, sans-serif;
  color: #444;
}
```

##### Nesting
- SCSS
```scss
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

- CSS

```css
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```

##### Partials

- e.g. `_partial.scss` 

##### Import

```SCSS
// _reset.scss
html,
body,
ul,
ol {
  margin:  0;
  padding: 0;
}
```
```SCSS
// base.scss
@import 'reset';
body {
  font: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

- CSS : Output

```CSS

html,
body,
ul,
ol {
  margin:  0;
  padding: 0;
}
body {
  font: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

##### Mixins

- SCSS

```SCSS

@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
.box { @include transform(rotate(30deg)); }

```
- CSS

```CSS

.box {
  -webkit-transform: rotate(30deg);
  -ms-transform: rotate(30deg);
  transform: rotate(30deg);
}

```

##### Extend/Inheritance






#### Refrences

- SASS Lang Guide : https://sass-lang.com/guide
