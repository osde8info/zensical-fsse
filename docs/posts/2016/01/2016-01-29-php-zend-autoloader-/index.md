---
title: "PHP ZEND autoloader code for Zend and Your classes"
date: 2016-01-29
categories: 
  - "fsse"
tags: 
  - "autoload"
  - "php"
  - "zend"
---

Simplest PHP ZEND autoloader code to autoload Zend classes and Your classes

```
<?php
require_once '/usr/lib/Zend/Loader/AutoloaderFactory.php';
require_once '/usr/lib/Zend/Loader/ClassMapAutoloader.php';

// ZEND CLASSES

$config = array(
    'Zend\Loader\StandardAutoloader' => array(
        'namespaces' => array(
            'Zend'      => '/usr/lib/Zend',
            'ZendXml'   => '/usr/lib/ZendXml',
        ),
    ),
);

Zend\Loader\AutoloaderFactory::factory($config);

// YOUR CLASSES

$loader = new Zend\Loader\ClassMapAutoloader();

// Register the class map:
$loader->registerAutoloadMap(__DIR__ . '/autoload_classmap.php');

// Register with spl_autoload:
$loader->register();
```
