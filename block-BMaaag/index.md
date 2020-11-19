writeCode

Write code to:-

- create a database named `mountains`

```
use mountains
```

- a collection inside that database named `himalayas`

```
db.createCollection("himalayas")
```

- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`

```
db.himalayas.insert({name: 'Dhauldhar range', height: '4000 mtrs'})
```

- insert multiple document using insertMany command

```
var himalayasInfo = [
 {
 name: "Mount Everst",
 height: "36000 mtr",
 },
 {
 name: "spiti valley",
 height: "6000 mtr",
 },
];

db.himalayas.insertMany(himalayasInfo)
```

- find all documents from mountains

```
db.himalayas.find()
```

- find a single document using name

```
db.himalayas.findOne()
```
