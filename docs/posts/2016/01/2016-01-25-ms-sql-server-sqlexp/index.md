---
title: "MS SQL Server SQLExpress 2014 TCP/IP"
date: 2016-01-25
categories: 
  - "fsse"
tags: 
  - "connection"
  - "db"
  - "ms"
  - "sql-express"
  - "sql-server"
  - "tcp-ip"
---

MS SQL Server 2014 SQL Express 2014 TCP/IP connections

SQL Server 2014 / SQL Express 2014

- Enable MS SQL Server TCP/IP connections
- Restart MS SQL Server
- Check MS SQL Server Log for port being used
- This may not be 1433 but might be 49445 instead
- Enable port through firewall

SQL Server Client

- Run Sql Server 2014 Managerment Studio
- Connect via Server Name or IP and specify Port after a comma
    - MYSERVER,1433
    - 10.10.10,10,49445
