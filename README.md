# Post-gres-practice-and-Notes

To login into psql command line tool:
psql -U username
select version();
select inet_server_port(), inet_server_servr();
select current_database();

## Restore

pg_restore: utility to store data from archive.

Steps:
  1. CREATE DATABASE dvdrental;
  2. Swicth to it using \c dvdrental


CMDS:

\l - list out dbs
\c dvdrental - switch to dvdrental db
Terms:
1. Table
2. Trigger
3. View
4. Function
5. Domain
6. Sequences
