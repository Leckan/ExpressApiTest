# ExpressApiTest

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# User Manager

This repository contains a simple demo API built with NodeJS.
The API is used to manage users in a MongoDB database.

### Development
This application was developed using [ExpressJS](http://expressjs.com/). MongoDB was used for persisting data with [Mongoose](https://mongoosejs.com/) as [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping).

### Installation
* Start up your terminal (or Command Prompt on Windows OS).
* Ensure that you've `node` installed on your PC.
* Clone the repository by entering the command `git clone https://github.com/Leckan/ExpressApiTest` in the terminal.
* Navigate to the project folder using `cd UserManager` on your terminal (or command prompt)
* After cloning, install the application's dependencies with the command `npm install`.
* Create a `.env` file in your root directory as described in `.env.sample` file. Variables such as DB_URL (which must be a mongoDB URL) and PORT are defined in the .env file and it is essential you create this file before running the application.
```
PORT=3000
DB_URL='mongodb://username:password@host:27017/databaseName'
```
* After this, you can then start the server with the command: `npm start`.

### Testing
To ensure that your installation is successful you'll need to run tests.
The command: `npm test` makes this possible. It isn't functional right now, but once it's done you'll be notified via the README.

### API Documentation
The API only has one endpoint which is the `/users` endpoint for saving users to the database. The endpoint works with the HTTP verbs: `POST`, `GET`, `PUT`, `DELETE`.

###### POST HTTP Request
-   `POST` /users
-   INPUT:
```x-form-url-encoded
name: Ahmed Mustapha
email: ahmed2real@gmail.com
password: password
```

###### HTTP Response

-   HTTP Status: `201: created`
-   JSON data
```json
{
  "_id": "5a36bf1ac436be0001a4bfec",
  "name": "Ahmed Mustapha",
  "email": "ahmed2real@gmail.com",
  "password": "password",
  "__v": 0
}
```

###### GET HTTP Response
-   `GET` /users

```json
[
    {
        "_id": "5a36bf1ac436be0001a4bfec",
        "name": "Ahmed Mustapha",
        "email": "ahmed2real@gmail.com",
        "password": "password",
        "__v": 0
    }
]
```

###### GET HTTP Response
-   `GET` /users/:id

```json
{
    "_id": "5a36bf1ac436be0001a4bfec",
    "name": "Ahmed Mustapha",
    "email": "ahmed2real@gmail.com",
    "password": "password",
    "__v": 0
}
```

###### DELETE HTTP Response
-   `DELETE` /users/:id

```json
User Ahmed Mustapha was deleted
```

###### POST HTTP Request
-   `PUT` /users/:id
-   INPUT:
```x-form-url-encoded
name: Ahmed Mustapha
email: ahmed2real@gmail.com
password: password
```

###### HTTP Response

-   HTTP Status: `200: OK`
-   JSON data
```json
{
	"_id":"5a36bf1ac436be0001a4bfec",
	"name":"Ahmed Mustapha",
	"email":"ahmed2real@gmail.com",
	"password":"password",
	"__v":0
}
```


###Reference Git Project
https://github.com/BolajiOlajide/UserManager


### Author
**Ahmed Mustapha** - Software Developer at Appzone
