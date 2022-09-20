# MongoDB CheatSheet

### All MongoDB commands you will ever need `MongoDb Cheatsheet`

We will see a comprehensive list of all the MongoDB commands you will ever need as a MongoDB beginner. This list covers almost all the most used commands in MongoDB.
I will assume that you are working inside a collection named `comments` on a MongoDB database of your choice

### 1. Database Commands
View all databases
```js
show dbs
```
Create a new or switch databases 
```js 
show dbs
```
View current Database

```js
db
```
Delete Database 

```js
db.dropDatabase()
```
### 2. Collection Commands
Show Collections
```js
show collections
```
Create a collection named `comments`
```js
db.createCollection('comments')
```
Drop a collection named `comments`
```js
db.comments.drop()
```



