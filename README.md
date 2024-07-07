# Post-gres-practice-and-Notes

To login into psql command line tool:
psql -U username
select version();
select inet_server_port(), inet_server_servr();
select current_database();

#### Restore backup from archive

pg_restore: utility to store data from archive.

Steps:
  1. Enter the terminal using psql -U username
  2. CREATE DATABASE dvdrental;
  3. Switch to it using \c dvdrental
  4. TODO: pg_restore -U postgres --dbname=dvdrental --verbose dvdrental.tar

#### Datatypes
1. Boolean
2. Characters
3. Numeric
(TODO practice on following data types)
4. UUID: serial: Generate RFC 4122 defined 128bits long UUID, provide better uniquenes then SERIAL. TODO ([RFC 4122](https://datatracker.ietf.org/doc/html/rfc4122))
5. Temporal - date, time, timestamp, timestampz and interval
6. JSON: json and jsonb 
7. Array
8. Net addr: inet, macaddr
9. point, line, lseg, box, polygon

###### 1. Boolean
To store boolean values, take either one of three. they are true, false or null

At the time insert 
0 and 1 , y and f, yes and no, t and f : are converted to true and false respectively.

###### 2. Characters:
1. CHAR(n): Padded space if value < n, issue error if more than n.
2. VARCHAR(n): Does not pad spaces, else same as CHAR(n)
3. TEXT: infinite length characters.

###### 3. Numeric
Two types
1. Integers
  1.a SMALLINT - 2 bytes can hold upto value equal to 32k.
  1.b INT - 4 bytes can hold value upto 2.14 billion.
  1.c SERIAL -  
2. Floating-point
  2.a float(n): 8byte - decimal number with, n number following decimal point.
  2.b real/float8 - 4byte
  3.b numeric(n, p) - decimal value with n digits before decimal point and p digits after decimal point.  
     
###### 4. Timezone
1. Date
2. Time
3. Timestamp
4. Tiemstampz
5. Interval

###### 5. JOSN
json: store json which need to be reparsed
jsonb: store json in binary format, faster to process and slow in insert and support index.

###### 6. UUID
above is enough

###### 
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
