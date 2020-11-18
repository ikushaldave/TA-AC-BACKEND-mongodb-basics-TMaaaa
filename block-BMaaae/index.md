writeCode

Write code to:-

- create a database named `sports`.

```
use sports
```

- list all databases present in local mongod server.

```
show dbs
```

- create 3 collections named `cricket`, `football`, `TT` in sports database.

```
db.createCollection("cricket")
db.createCollection("football")
db.createCollection("tt")
```

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.

```
db.cricket.insertMany([{"name": "Yugal", "age": 18, "email": "yugal@xyz.com", "bid_price": 300}])

db.football.insertMany([{"name": "itzme", "age": 23, "email": "itzme@xyz.com", "bid_price": 123}])

db.tt.insertMany([{"name": "random", "age": 27, "email": "random@xyz.com", "bid_price": 150}])
```

- list all collections in sports database.

```
show collections
```

- rename `TT` collection to `tennis`.

```
db.tt.renameCollection("tennis")
```

- create a capped collection called `khokho` which should have max 3 documents.
  Try inserting more than 3 and see what happens?

```
db.createCollection("khokho", {capped: true, size: 1024, max: 3})

db.khokho.insertMany([{"name": "Yugal", "age": 18, "email": "yugal@xyz.com", "bid_price": 300},
{"name": "itzme", "age": 23, "email": "itzme@xyz.com", "bid_price": 123},
{"name": "random", "age": 27, "email": "random@xyz.com", "bid_price": 150}])

db.khokho.insert({"name": "Kushal", "age": 23, "email": "kushal@xyz.com", "bid_price": 600})


// it delete the old document from top and insert new document at bottom
```

- check whether a collection is capped or not?

```
db.khokho.isCapped() // true
db.football.isCapped() // false
```

- drop all documents from `football` collection.

```
db.football.drop()
```

- delete cricket collection completely.

```
db.cricket.remove({})
```

- delete sports database.

```
db.dropDatabase()
```

- check which database you are connected to ?

```
db
```

- connect to test database

```
use test
```