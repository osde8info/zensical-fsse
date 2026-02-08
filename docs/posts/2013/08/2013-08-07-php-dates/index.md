---
title: "#php #dates"
date: 2013-08-07
categories: 
  - "fsse"
tags: 
  - "date"
  - "datetime"
  - "php"
  - "webdev"
---

how to add a year to a php date

PHP ALL

```
$oneyear = strtotime("+1 year");
```

PHP 5.2

```
$date = getdate();
$oneyear = mktime(
        $date['hours'],$date['minutes'],$date['seconds'],
        $date['mon'],$date['mday'],$date['year']+1
    );
echo $oneyear;
echo PHP_EOL;
```

PHP 5.3

```
$oneyear = date_timestamp_get(
    date_add(date_create(),
        date_interval_create_from_date_string('1 year')));
echo $oneyear;
echo PHP_EOL;
```
