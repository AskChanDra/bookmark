# Node JS REST

- Install Express

```bash
npm install express --save

```

- Create `app.js` file:

```javascript

var express = require("express");
var app = express();

app.listen(3000, () => {
  console.log("Server running at port 3000");
});

app.get("/users", (req, res, next) => {
  res.json(["Tony", "Lisa", "Michael", "Ginger", "Food"]);
});
```


- Run on CMD

```bash
node app.js
```

- Via Postman Tool: 
- `GET` : http://localhost:3000/users
- Response :

```json
[
    "Tony",
    "Lisa",
    "Michael",
    "Ginger",
    "Food"
]
```
