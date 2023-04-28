# RESTful API

This is a RESTful API example based on Node.js and MongoDB, following the **MVC pattern** i.e. Model ~~View~~ Controller.

**Mongoose** is used for Database transactions which is an elegant solution to mongodb object modeling for node.js.

The application is **production ready**, and can be used behind a Nginx reverse proxy securely.

---

#### To start setting up the project

Step 1: Clone the repo

Step 2: cd into the cloned repo and run:

```bash
npm install
```

Step 3: Put your credentials in the .env file.

```bash
PORT=3000
MONGODB_URI=YOUR MONGODB URI
DB_NAME=DATABASE NAME OF YOUR CHOICE
DB_USER=DATABASE USER
DB_PASS=DATABASE USER PASSWORD 
```

e.g:

PORT=3000
MONGODB_URI=mongodb://127.0.0.1:27017
DB_NAME=admin
DB_USER=admin
DB_PASS=admin


Step 4: Start the API by

```bash
npm start
```

## To Start MongoDB


To run service, simply run the following command:
```
brew services start mongodb-community
brew services stop mongodb-community
brew services restart mongodb-community
```


<br/><br/>

This command is for apple M1:
```
sudo mongod --config /opt/homebrew/etc/mongod.conf
sudo mongod --config /opt/homebrew/etc/mongod.conf —-fork
```

In another terminal, run:
`mongosh`


## To create username and password
```
use admin 

db.createUser( { 
  user: "user_name", 
  pwd: "user_pass", 
  roles: [ { role: "userAdminAnyDatabase", db: "admin" }, { role: "readWriteAnyDatabase", db: "admin" }, { role: "dbAdminAnyDatabase", db: "admin" } ] 
})
```

## To show DBS

```
show dbs
```


