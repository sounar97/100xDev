#Basics
test> show dbs
Student   8.00 KiB
admin    40.00 KiB
config   72.00 KiB
local    72.00 KiB
##Creating Database
test> use school
switched to db school
school> db.createCollection("Students")
{ ok: 1 }
school> show dbs
admin   40.00 KiB
config  72.00 KiB
local   72.00 KiB
school   8.00 KiB
#Inserting data 
db.Students.insertOne({name:"Sourav",age:21})
{
  acknowledged: true,
  insertedId: ObjectId('669831c21425a8e751c4e49b')
}
school> db.Students.find()
[
  {
    _id: ObjectId('669831c21425a8e751c4e49b'),
    name: 'Sourav',
    age: 21
  }
]
school> db.Students.insertMany({name:"abc",age:21},{name:"def",age:20},{name:"ghi",age:22})
MongoInvalidArgumentError: Argument "docs" must be an array of documents
school> db.Students.insertMany([{name:"abc",age:21},{name:"def",age:20},{name:"ghi",age:22}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('669832dd1425a8e751c4e49c'),
    '1': ObjectId('669832dd1425a8e751c4e49d'),
    '2': ObjectId('669832dd1425a8e751c4e49e')
  }
}
