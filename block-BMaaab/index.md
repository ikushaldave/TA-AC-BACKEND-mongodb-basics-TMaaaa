writeCode

Run these shell commands in mongo shell:

- db.version()
- db.stats()
- db.help()

Write code to

- create a database of your country name.
- check list of databases to see newly created database.
- check which database you are currently connected to ?


```
use india

// Use to switch to database or to create new db if it not available it will be not visible until it has min 1 collection or document


db.createCollection("Delhi")

// {"ok": 1}


show dbs

// To see the list of all databases we use show dbs

db

// To see what db I am currently onw
```