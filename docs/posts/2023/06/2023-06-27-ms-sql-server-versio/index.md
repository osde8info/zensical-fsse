---
title: "MS SQL Server Versions"
date: 2023-06-27
categories: 
  - "fsse"
---

How do you find out ?

```
select @@VERSION

or

SELECT SERVERPROPERTY('productversion'), SERVERPROPERTY ('productlevel'), SERVERPROPERTY ('edition')
```

Versions

- 14.x is sql server 2017

- 15.x is sql server 2019

- 16.x is sql server 2022

See

- https://learn.microsoft.com/en-us/troubleshoot/sql/releases/find-my-sql-version

- https://learn.microsoft.com/en-us/troubleshoot/sql/releases/faq-acronyms
