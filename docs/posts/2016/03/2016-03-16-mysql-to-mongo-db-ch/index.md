---
title: "#MySQL to #Mongo DB check min reqs before you swap #dba"
date: 2016-03-16
categories: 
  - "fsse"
tags: 
  - "database"
  - "dba"
  - "mongo"
---

In order to avoid the Mongo DB error

```
WARNING: soft rlimits too low.
```

Mongo DB needs rlimits set to

- 1024 processes
- 64000 files
- Number of processes should be at least 32000 (0.5 times number of files)

So follow these instructions

- https://docs.mongodb.org/manual/reference/ulimit/
