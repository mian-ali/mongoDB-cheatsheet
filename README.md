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
use dbName
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
### 3. Row(Document) Commands
Show all Rows in a Collection 
```js
db.comments.find()
```
Show all Rows in a Collection (Prettified)
```js
db.comments.find().pretty()
```
Find the first row matching the object
```js
db.comments.findOne({name: 'Ahmad'})
```
Insert One Row
```js
db.comments.insert({
    'name': 'Ahmad',
    'lang': 'JavaScript',
    'member_since': 5
 })
```
Insert many Rows
```js
db.comments.insertMany([{
    'name': 'Ahmad',
    'lang': 'JavaScript',
    'member_since': 5
    }, 
    {'name': 'test',
    'lang': 'Python',
    'member_since': 3
    },
    {'name': 'ali',
    'lang': 'Java',
    'member_since': 4
}])

```
Search in a MongoDb Database
```js
db.comments.find({lang:'Python'})
```
Limit the number of rows in output
```js
db.comments.find().limit(2)
```
Count the number of rows in the output
```js
db.comments.find().count()
```
Update a row
```js
db.comments.updateOne({name: 'Ali'},
{$set: {'name': 'Ahmad',
    'lang': 'JavaScript',
    'member_since': 51
}}, {upsert: true})
```
Mongodb Increment Operator
```js
db.comments.update({name: 'Rohan'},
{$inc:{
    member_since: 2
}})
```
Mongodb Rename Operator
```js
db.comments.update({name: 'Rohan'},
{$rename:{
    member_since: 'member'
}})
```
Delete Row 
```js
db.comments.remove({name: 'Ahmad'})
```
Less than/Greater than/ Less than or Eq/Greater than or Eq
```js
db.comments.find({member_since: {$lt: 90}})
```
```js 
db.comments.find({member_since: {$lte: 90}})
```
```js
db.comments.find({member_since: {$gt: 90}})
```
```js
db.comments.find({member_since: {$gte: 90}})
```
