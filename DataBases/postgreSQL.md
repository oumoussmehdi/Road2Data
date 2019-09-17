- connect using psql (cmd or application)
- click ok for default values or specify the desired server 
- cmd : # psql -h localhost -p 5432 -U postgress testdb

### show databases
- select datname from pg_database;
- \l 

### connect to db_name
- \c db_name

### show tables:
\dt
or 
SELECT * FROM pg_catalog.pg_tables;

ref: 
* https://www.tutorialspoint.com/postgresql/postgresql_create_table.htm
