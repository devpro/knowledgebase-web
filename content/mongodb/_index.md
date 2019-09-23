---
title: "MongoDB"
date: 2019-08-22T18:51:00+02:00
draft: false
weight: 60
pre: "<i class='fa fa-leaf'></i> "
---

MongoDB is a cross-platform document-oriented database technology, part of the NoSQL family, storing data in a JSON-like format.

See [mongodb.com](https://www.mongodb.com/), [GitHub](https://github.com/mongodb), [Twitter](https://twitter.com/MongoDB).

## Content

{{% children sort="Name" %}}

## Presentation

![image.png](/images/attachments/image-10d40ef9-5b8e-400b-b600-602cbb49d98b.png)

## Learn

See [Engineering Journal](https://engineering.mongodb.com/), [SlideShare](https://www.slideshare.net/MongoDB), [Videos](https://www.mongodb.com/presentations).

### Product offering

- [Cloud Data Strategy](https://www.mongodb.com/initiatives/cloud-data-strategy)
- [Mobile](https://www.mongodb.com/products/mobile)
- Stitch: Serverless platform

### Key features

- Flexible schema
- Performance
- High Availability
  - Primary / Secondaries architecture
- BSON storage (Binary JSON)
  - [GeoJSON Objects](https://docs.mongodb.com/manual/reference/geojson/) support of [GeoJson format](http://geojson.org/) for encoding a variety of geographic data structures
- ACID transactions
  - [The cost of MongoDB ACID transactions in theory and practice](http://henrikingo.github.io/presentations/Highload%202018%20-%20The%20cost%20of%20MongoDB%20ACID%20transactions%20in%20theory%20and%20practice/index.html#/markdown)

#### Replication

[Manual](https://docs.mongodb.com/manual/replication/)

A _replica set_ is a group of `mongod` processes that maintain the same data set. Replica sets provide redundancy and high availability.

A node of the replica set can be: Primary, Secondary, Arbitrer.

##### Read preference

[Manual](https://docs.mongodb.com/manual/core/read-preference/)

##### Write concern

[Manual](https://docs.mongodb.com/manual/reference/write-concern/)

##### Read concern

[Manual](https://docs.mongodb.com/manual/reference/read-concern/)

#### Indexing

[Manual](https://docs.mongodb.com/manual/indexes/) [Query Plans](https://docs.mongodb.com/manual/core/query-plans/) [Limits](https://docs.mongodb.com/manual/reference/limits/#indexes) [Analyze Query Performance](https://docs.mongodb.com/manual/tutorial/analyze-query-plan/)

MongoDB indexes use a [B-tree](https://en.wikipedia.org/wiki/B-tree) data structure.

Indexes gets have better read time but have an impact on write time.

Index Types:

- Single Field
- Compound Index
- Multikey Index
- Geospatial Index
- Text Indexes
- Hashed Indexes

Index Properties:

- Unique Indexes
- Partial Indexes
- Sparse Indexes
- TTL Indexes (Time To Live)

#### Performance

[Manual](https://docs.mongodb.com/manual/administration/analyzing-mongodb-performance/)

#### Storage engine

The storage engine that is used can be seen with the command `db.serverStatus()`. It is a `mongod` option: `--storageEngine`.

In March 2015, there were two choices: MMAPv1 (original) and WiredTiger (new).

**Wired Tiger** is new in MongoDB 3.0. It is the first pluggable storage engine.

Features:

- Document level locking
- Compression
  - Snappy (default) - fast
  - Zlib - more compression
  - None
- Lacks some pitfalls of MMAPv1
- Performance gains

Background:

- Built separately from MongoDB
- Used by other's DB
- Open source

Internals:

- Stores data in btrees
- Writes are initially separate, incorporated later
- Two caches
  - WT caches - 1/2 of RAM (default)
  - FS cache
- Checkpoint: every minute or more
- No need for a journal

#### Transactions

- [Presentation](https://www.mongodb.com/transactions)
- [Documentation](https://docs.mongodb.com/manual/core/transactions/)

### Recipes

- Store large data: [GridFS](https://docs.mongodb.com/manual/core/gridfs/)
  - [mongofiles](https://docs.mongodb.com/manual/reference/program/mongofiles)
  - [Building MongoDB Applications with Binary Files Using GridFS](https://www.mongodb.com/blog/post/building-mongodb-applications-binary-files-using-gridfs-part-1)

## Tools

### Compass

- [Creating Compass Plugins](https://docs.mongodb.com/compass/master/plugins/creating-compass-plugins/)
- [Transpiling between any programming languages (Part 1)](https://engineering.mongodb.com/post/transpiling-between-any-programming-languages-part-1)
