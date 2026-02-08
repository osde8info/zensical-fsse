---
title: "mongo mongoshell query examples"
date: 2016-06-22
categories: 
  - "fsse"
tags: 
  - "db"
  - "dba"
  - "mongo"
  - "query"
---

mongo mongoshell query examples

```
db.MYTABLE.find()
```

```
db.MYTABLE.find({}).count
```

```
db.MYTABLE.find({}).limit(10)
```

```
db.MYTABLE.find({"name":"a"})
```

```
db.MYTABLE.find({"name":"a"},{name:1})
```

```
db.MYTABLE.find({"name":"a"}).sort({name:1})
```

```
db.MYTABLE.remove({"name":"a"})
```
