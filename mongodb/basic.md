
# MongoDB

### Start
```sh
  cd C:\Program Files\MongoDB\Server\4.4\bin
  mongod.exe --dbpath "C:\data" 
 ```
 ```sh
  cd C:\Program Files\MongoDB\Server\4.4\bin
  mongo.exe 
 ```
 ### Create or Dropdatabse
 - show dbs
 - use mydb  ---->for create new ddb
 - db.dropDatabase
To see the current database type-> db
 
### createCollection()
-  show collections  ----> [for show all the collection in that db]
 - db.createCollection(name, options)
 - db.createCollection("mycollection")
 - db.mycollection.drop()
 
 
```sh
>>  use mydb
    switched to db mydb
>>  show collections
    mycol
    mycollection
    system
    mycol2
>>  db.mycollection.drop()
    true
 ```

### insert() 
  - db.COLLECTION_NAME.insert(document)
  -  db.MYCol.insert({"namme":"Souvik biswas","Age":"23"});
  - db.COLLECTION_NAME.insertOne(document)
  -  db.empDetails.insertMany(array of documents)
 
### find() 
   - db.COLLECTION_NAME.find()
   - db.COLLECTION_NAME.find().pretty()
   

|Operation | Syntax | Example | RDBMS Equivalent |
| ------ | ------ | ------ |  ------ |
|Equality| {<key>:{$eg;<value>}}| db.mycol.find({"by":"tutorials point"}).pretty()|where by = 'tutorials point'
|Less Than|{<key>:{$lt:<value>}}|db.mycol.find({"likes":{$lt:50}}).pretty()|where likes < 50|
|Less Than Equals|{<key>:{$lte:<value>}}|db.mycol.find({"likes":{$lte:50}}).pretty()|where likes <= 50|
|Greater Than| {<key>:{$gt:<value>}}| db.mycol.find({"likes":{$gt:50}}).pretty()| where likes > 50|
|Greater Than Equals|{<key>:{$gte:<value>}}|db.mycol.find({"likes":{$gte:50}}).pretty()|where likes >= 50|
|Not Equals|	{<key>:{$ne:<value>}}|db.mycol.find({"likes":{$ne:50}}).pretty()|where likes != 50|
|Values in an array|{<key>:{$in:[<value1>, <value2>,……<valueN>]}}|db.mycol.find({"name":{$in:["Raj", "Ram", "Raghu"]}}).pretty()|Where name matches any of the value in :["Raj", "Ram", "Raghu"]|
|Values not in an array|{<key>:{$nin:<value>}}|db.mycol.find({"name":{$nin:["Ramu", "Raghav"]}}).pretty()|Where name values is not in the array :["Ramu", "Raghav"] or, doesn’t exist at all|

#### AND 
 - db.mycol.find({ $and: [ {<key1>:<value1>}, { <key2>:<value2>} ] })
 -  db.mycol.find({$and:[{"by":"tutorials point"},{"title": "MongoDB Overview"}]}).pretty();

#### OR
- >db.mycol.find(
   {
      $or: [
         {key1: value1}, {key2:value2}
      ]
   }
).pretty()

- db.mycol.find({$or:[{"by":"tutorials point"},{"title": "MongoDB Overview"}]}).pretty()


#### AND and OR 
- Equivalent SQL where clause is 'where likes>10 AND (by = 'tutorials point' OR title = 'MongoDB Overview')'


```sh
db.mycol.find({"likes": {$gt:10}, $or: [{"by": "tutorials point"},
   {"title": "MongoDB Overview"}]}).pretty()
```







