#service

# TCP3306 - MySQL
## What is TCP3306 - MySQL?
MySQL is a database server, usually servers today run MariaDB instead, since it's an open fork of MySQL.

## How do I connect to TCP3306 - MySQL?
`mysql -u <username> -p [-h <IP>]`

## Any documentation on TCP3306 - MySQL?
Look up `mysql` online, you'll find plenty.

## How do I collect info from TCP3306 - MySQL?
After logging in successfully, you should run a full scan of the tables on the DB and find out how to access them.
```sql
use information_schema;
SELECT DISTINCT table_schema from tables; -- Gives all DBs in server
SELECT DISTINCT table_name from tables WHERE table_schema="<DB_NAME>" -- Gives all tables in DB.
```

## How do I run code on TCP3306 - MySQL?
[CVE-2021-27928](https://www.exploit-db.com/exploits/49765) - On MariaDB 10
* Make sure to use `linux/x64/shell_reverse_tcp` on this one! An `x86` file won't execute!

UDF_RAPTOR - a User-Defined Function that runs code.
* Uses an SO file to run a custom function in SQL -> native code.[]()