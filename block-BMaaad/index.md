writeCode

Write command to

- List collections from a database.

```
show collection
```

- create a new collection in your country database which you created recently.

```
db.createCollections("state")
```

Write code to:-

- crate a database named `weather`

```
use weather
```

- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.

```
db.createCollection("temperature", {size: 1000000, max: 3, capped: true})

db.temperature.insertMany([{"date": "18-11-2020", "temp": "32"}, {"date": "19-11-2020", "temp": "38"}, {"date": "20-11-2020", "temp": "2"}])

db.temperature.insert({"date": "30-11-2020", "temp": "22"})

// Inserting more than max or size the older document get deleted by mongoDB and size as high priority than max
```

- create a simple collection named `humidity`

```
db.createCollection("humidity")
```

- check whether `temperature` collection is capped or not ?

```
db.temperature.stats()
```

- Delete `humidity` collection and then the entire database(weather).

```
db.humidity.drop()
db.dropDatabase()
```