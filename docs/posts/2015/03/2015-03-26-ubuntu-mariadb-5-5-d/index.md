---
title: "ubuntu mariadb 5.5 doesnt install with mysql 5.6 libraries"
date: 2015-03-26
categories: 
  - "fsse"
tags: 
  - "aptitude"
  - "mariadb"
  - "mysql"
---

uninstall mysql 5.6 and force install of older version of mysql

```
see old versions available
# aptitude versions mysql-common

force older version of mysql
# aptitude install mysql-common=5.5.41-0ubuntu0.14.04.1

prevent mysql-common updating (hold it via '=')
# aptitude install mysql-common=

install mariadb
# aptitude install mariadb-server
```

verify

```
# dpkg -l | grep ii | egrep "mysql|maria"
ii  libmariadbclient18:amd64                  5.5.41-1ubuntu0.14.04.1                  amd64        MariaDB database client library
ii  libmysqlclient18:amd64                    5.5.41-0ubuntu0.14.04.1                  amd64        MySQL database client library
ii  mariadb-client-5.5                        5.5.41-1ubuntu0.14.04.1                  amd64        MariaDB database client binaries
ii  mariadb-client-core-5.5                   5.5.41-1ubuntu0.14.04.1                  amd64        MariaDB database core client binaries
ii  mariadb-common                            5.5.41-1ubuntu0.14.04.1                  all          MariaDB common metapackage
ii  mariadb-server                            5.5.41-1ubuntu0.14.04.1                  all          MariaDB database server (metapackage depending on the latest version)
ii  mariadb-server-5.5                        5.5.41-1ubuntu0.14.04.1                  amd64        MariaDB database server binaries
ii  mariadb-server-core-5.5                   5.5.41-1ubuntu0.14.04.1                  amd64        MariaDB database core server files
ii  mysql-apt-config                          0.3.3-2ubuntu14.04                       all          Auto configuration for MySQL APT Repo.
ii  mysql-common                              5.5.41-0ubuntu0.14.04.1                  all          MySQL database common files, e.g. /etc/mysql/my.cnf
ii  mysql-workbench-community                 6.2.5-1ubu1404                           amd64        MySQL Workbench
ii  php5-mysql                                5.5.9+dfsg-1ubuntu4.7                    amd64        MySQL module for php5

```
