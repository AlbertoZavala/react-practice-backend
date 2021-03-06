# Mern-Backend

## Requirements

#### Node:
First of all, we have to install Node.js from [here](https://nodejs.org/es/). Express is an environment for work with javascript on sidesirver.

#### MongoDB:
We need to install MongoDB from [here](https://www.mongodb.com/try/download/community)
We have to create a .env file on root of application (on MERN-BACKEDN) and here, we gonna set up the URI connection to mongo database.

    MONGODB_URI=mongodb://localhost/{databasename}

If you don't set this variable, it will be connect to testdatabase by default.

    PORT={portnumber}

If PORT does not exist, application will take port 4000 by default

## Principal dependencies

#### Express
Description in here...

#### Mongoose        
Description in here... This is an ORM for use it with MongoDB

#### Cors
Description in here... This is for comunication between servers

#### Dotenv
Description in here... This is for set environments variables

    npm i express mongoose cors dotenv

## Others tools

#### Nodemon
Description in here... With this, server will restart every time that a change is detected on code.

    npm i nodemon -D

The -D word is for keep nodemon outside of dependencies on package.json. This will be added on devDependencies.

## Run server

Originally, to start the server, we need to run:

    node src/index.js

But, as we want to use Nodemon to restart the server every code change, I do add the next line to the ***scritps***
into package json:

    "dev": "nodemon src/index.js"

So, with this, now to start the server, we have to run 

    npm run dev

Then we can go to the navigator and go to localhost:3000


---
# API

#### Headers
First at all, we should use: 
KEY

    Content-Type

VALUE

    application/json

## Users

#### GET - Get all users
    http://localhost:{port}/api/users

#### GET - Get one user
    http://localhost:{port}/api/users/5f9e53250988343778083c8c

#### PUT - Update one user
    http://localhost:{port}/api/users/5f9e53250988343778083c8c

Body
```
    {    
        "username": "Updated User Name"    
    }
```

#### POST - Create one user
    http://localhost:{port}/api/users/

Body
```
    {    
        "username": "User Name"    
    }
```

#### DELETE - Delete one user
    http://localhost:{port}/api/users/5f9e53250988343778083c8c

## Notes

#### GET - Get all notes
    http://localhost:{port}/api/notes

#### GET - Get one note
    http://localhost:{port}/api/notes/5f9e53250988343778083c8c

#### PUT - Update one note
    http://localhost:{port}/api/notes/5f9e53250988343778083c8c

```
{    
    "title": "Updated Title",
    "content": "Updated content text",    
    "author": "Updated Author Name Here"
}
```

#### POST - Create one note
    http://localhost:{port}/api/notes/

Body        

```
{    
    "title": "Title",
    "content": "This is my first note",    
    "author": "Author Name Here"
}
```

#### DELETE - Delete one note
    http://localhost:{port}/api/notes/5f9e53250988343778083c8c

