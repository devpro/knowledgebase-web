---
title: "Command Cheatsheet"
date: 2019-11-25T14:24:23+01:00
draft: false
weight: 22
---

- Switch database: `use database_name`
- Get info on current database: `db`
- See all databases: `show dbs`
- Drop a database: `db.dropDatabase()`
- See all collections: `show collections`
- Create a collection: `db.createCollection("name", "options")`
- Delete a collection: `db.collection_name.drop()`
- Insert data: `db.collection_name.insert({...})`
- Update data: `db.collection_name.update({_id: ObjectId("...")}, {...})`
- Find data: `db.collection_name.find({...}).pretty()`
- Remove data: `db.collection_name.remove({...})`
