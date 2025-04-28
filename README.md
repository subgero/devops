# How to become a Devops Engineer

## Create a Rest API

Create a new directory 

```
mkdir rest-api
```

Enter to the new directory
```
cd rest-api
```

Initialize a new Node.js app
```
npm init
```

Install Express.js

```
npm install express dotenv
```

Create file env
```
PORT = 500
```
Add the next line to the package.json file:

```
"type": "module",
```

Add the next line in the scripts section in the package.json file:

```
"start": "node index.js"
```

Create a new index.js file and put this content in that file:

```
import express from 'express';
import dotenv from 'dotenv';

dotenv.config();

const app = express ();


app.use(express.json());

const PORT = process.env.PORT || 5000;


app.listen(PORT, () =>{
    console.log("Server listening on port:", PORT);
});

app.get("/", (req, res) => {

    res.json({"message":"Hola mundo"});

});
```

Now run:

```
npm run start
```
