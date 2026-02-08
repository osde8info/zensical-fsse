---
title: "#php #mysql #pdo prepare and single quotes #gotcha"
date: 2015-09-07
categories: 
  - "fsse"
tags: 
  - "mysql"
  - "pdo"
  - "php"
---

i suspect that php pdo prepare may be double escaping single quotes in your sql string so replace single quotes with double quotes

FAILS

```
$sql = <<<EOT
    select * from cars where colour='red'
EOT;
$stm = $db->prepare($sql);

```

WORKS

```
$sql = <<<EOT
    select * from cars where colour="red"
EOT;
$stm = $db->prepare($sql);
```
