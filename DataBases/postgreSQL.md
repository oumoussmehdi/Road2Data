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

### migrate db from a server to another:
- pg_dump
- pgAdmin : backup origin > restore target

### show the row count of the different tables:
```sql
SELECT schemaname,relname,n_live_tup 
  FROM pg_stat_user_tables 
  ORDER BY n_live_tup DESC;
```

ref: 
* https://www.tutorialspoint.com/postgresql/postgresql_create_table.htm
