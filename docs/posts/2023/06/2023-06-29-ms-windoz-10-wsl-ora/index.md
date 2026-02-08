---
title: "ms windoz 10 &amp; wsl &amp; oraclelinux 8 &amp; ms sql server 19 hacks"
date: 2023-06-29
categories: 
  - "fsse"
---

ms windoz 10 & wsl & oraclelinux 8 & ms sql server 19 install hacks

add repos

```
curl -o /etc/yum.repos.d/mssql-server.repo \ https://packages.microsoft.com/config/rhel/8/mssql-server-2019.repo

curl https://packages.microsoft.com/config/rhel/8/prod.repo > /etc/yum.repos.d/msprod.repo
```

install mssql

```
dnf install mssql-server
dnf install mssql-tools
```

setup

```
/opt/mssql/bin/mssql-conf setup

[3 = Express]
```

msql server installer may NOT create an openssl cert so you may need to setup one manually

```
openssl req -x509 -nodes -newkey rsa:2048 -subj '/CN=MYHOSTNAME' \
-keyout mssql.key -out mssql.pem -days 365 

chown mssql:mssql mssql.key mssql.pem 

mv mssql.pem /etc/ssl/certs/ 

mkdir /etc/ssl/private/

mv mssql.key /etc/ssl/private/
```

edit/update mssql.conf

```
systemctl stop mssql-server 

cat /var/opt/mssql/mssql.conf 

/opt/mssql/bin/mssql-conf set network.tlscert /etc/ssl/certs/mssql.pem 
/opt/mssql/bin/mssql-conf set network.tlskey /etc/ssl/private/mssql.key 
/opt/mssql/bin/mssql-conf set network.tlsprotocols 1.2 
/opt/mssql/bin/mssql-conf set network.forceencryption 0 

cat /var/opt/mssql/mssql.conf 

systemctl restart mssql-server 

```

check status

```
systemctl status mssql-server 
```

check you can login WITHOUT cert check

```
sqlcmd -C -U sa -P
```

enable CA

```
cp cert to /etc/pki/ca-trust/source/anchors/ 
then use update-ca-trust to enable it as system CA certificate.
```

open firewall

```
sudo firewall-cmd --zone=public --add-port=1433/tcp --permanent
sudo firewall-cmd --reload
```

refs

- https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-configure-mssql-conf?view=sql-server-ver16

- https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-red-hat?view=sql-server-linux-ver15&preserve-view=true

- [https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-encrypted-connections?view=sql-server-ver16](https://learn.microsoft.com/en-us/sql/linux/sql-server-linux-encrypted-connections?view=sql-server-ver16)

- https://support.microsoft.com/en-us/topic/kb4052969-fix-minimum-memory-limit-set-to-2gb-to-install-or-start-sql-server-2017-e7d95b55-7106-bf95-e82a-ae1fe8c21479
