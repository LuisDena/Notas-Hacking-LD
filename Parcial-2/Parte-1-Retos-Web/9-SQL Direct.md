# SQL Direct
## Objetivo
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.
`psql -h saturn.picoctf.net -p 56508 -U postgres pico`Password is `postgres`
## Pistas

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
--------------------------------------------------
Enter your picoCTF username: Dena
Enter your picoCTF password (characters will be hidden): 

==========================================================================

Welcome to the picoCTF webshell!

💻  The webshell is intended only for solving picoCTF challenges. Any
   other usage is a violation of our terms and conditions.

📹  Sessions are monitored and logged to prevent abuse. Please do not
   enter any sensitive information into the webshell.

🗄  Files stored outside of your home directory will not persist between
   webshell sessions.

🌐  Network connectivity and resources are limited. Some limits can be
   checked by typing usage.

😴  Idle sessions will automatically log out after 15 minutes.

📚  For more information and a beginner's guide, type less ~/README.txt.

==========================================================================

dena-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 56508 -U postgres pico
Password for user postgres: 
psql: error: connection to server at "saturn.picoctf.net" (13.59.203.175), port 56508 failed: FATAL:  password authentication failed for user "postgres"
dena-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 56508 -U postgres pico
Password for user postgres: 
psql (14.5 (Ubuntu 14.5-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# help
You are using psql, the command-line interface to PostgreSQL.
Type:  \copyright for distribution terms
       \h for help with SQL commands
       \? for help with psql commands
       \g or terminate with semicolon to execute query
       \q to quit
pico=# \h
Available help:
  ABORT                            ALTER TEXT SEARCH TEMPLATE       CREATE PUBLICATION               DROP FUNCTION                    IMPORT FOREIGN SCHEMA
  ALTER AGGREGATE                  ALTER TRIGGER                    CREATE ROLE                      DROP GROUP                       INSERT
  ALTER COLLATION                  ALTER TYPE                       CREATE RULE                      DROP INDEX                       LISTEN
  ALTER CONVERSION                 ALTER USER                       CREATE SCHEMA                    DROP LANGUAGE                    LOAD
  ALTER DATABASE                   ALTER USER MAPPING               CREATE SEQUENCE                  DROP MATERIALIZED VIEW           LOCK
  ALTER DEFAULT PRIVILEGES         ALTER VIEW                       CREATE SERVER                    DROP OPERATOR                    MOVE
  ALTER DOMAIN                     ANALYZE                          CREATE STATISTICS                DROP OPERATOR CLASS              NOTIFY
  ALTER EVENT TRIGGER              BEGIN                            CREATE SUBSCRIPTION              DROP OPERATOR FAMILY             PREPARE
  ALTER EXTENSION                  CALL                             CREATE TABLE                     DROP OWNED                       PREPARE TRANSACTION
  ALTER FOREIGN DATA WRAPPER       CHECKPOINT                       CREATE TABLE AS                  DROP POLICY                      REASSIGN OWNED
  ALTER FOREIGN TABLE              CLOSE                            CREATE TABLESPACE                DROP PROCEDURE                   REFRESH MATERIALIZED VIEW
  ALTER FUNCTION                   CLUSTER                          CREATE TEXT SEARCH CONFIGURATION DROP PUBLICATION                 REINDEX
  ALTER GROUP                      COMMENT                          CREATE TEXT SEARCH DICTIONARY    DROP ROLE                        RELEASE SAVEPOINT
  ALTER INDEX                      COMMIT                           CREATE TEXT SEARCH PARSER        DROP ROUTINE                     RESET
  ALTER LANGUAGE                   COMMIT PREPARED                  CREATE TEXT SEARCH TEMPLATE      DROP RULE                        REVOKE
  ALTER LARGE OBJECT               COPY                             CREATE TRANSFORM                 DROP SCHEMA                      ROLLBACK
  ALTER MATERIALIZED VIEW          CREATE ACCESS METHOD             CREATE TRIGGER                   DROP SEQUENCE                    ROLLBACK PREPARED
  ALTER OPERATOR                   CREATE AGGREGATE                 CREATE TYPE                      DROP SERVER                      ROLLBACK TO SAVEPOINT
  ALTER OPERATOR CLASS             CREATE CAST                      CREATE USER                      DROP STATISTICS                  SAVEPOINT
  ALTER OPERATOR FAMILY            CREATE COLLATION                 CREATE USER MAPPING              DROP SUBSCRIPTION                SECURITY LABEL
  ALTER POLICY                     CREATE CONVERSION                CREATE VIEW                      DROP TABLE                       SELECT
  ALTER PROCEDURE                  CREATE DATABASE                  DEALLOCATE                       DROP TABLESPACE                  SELECT INTO
  ALTER PUBLICATION                CREATE DOMAIN                    DECLARE                          DROP TEXT SEARCH CONFIGURATION   SET
  ALTER ROLE                       CREATE EVENT TRIGGER             DELETE                           DROP TEXT SEARCH DICTIONARY      SET CONSTRAINTS
  ALTER ROUTINE                    CREATE EXTENSION                 DISCARD                          DROP TEXT SEARCH PARSER          SET ROLE
  ALTER RULE                       CREATE FOREIGN DATA WRAPPER      DO                               DROP TEXT SEARCH TEMPLATE        SET SESSION AUTHORIZATION
  ALTER SCHEMA                     CREATE FOREIGN TABLE             DROP ACCESS METHOD               DROP TRANSFORM                   SET TRANSACTION
  ALTER SEQUENCE                   CREATE FUNCTION                  DROP AGGREGATE                   DROP TRIGGER                     SHOW
  ALTER SERVER                     CREATE GROUP                     DROP CAST                        DROP TYPE                        START TRANSACTION
  ALTER STATISTICS                 CREATE INDEX                     DROP COLLATION                   DROP USER                        TABLE
  ALTER SUBSCRIPTION               CREATE LANGUAGE                  DROP CONVERSION                  DROP USER MAPPING                TRUNCATE
  ALTER SYSTEM                     CREATE MATERIALIZED VIEW         DROP DATABASE                    DROP VIEW                        UNLISTEN
  ALTER TABLE                      CREATE OPERATOR                  DROP DOMAIN                      END                              UPDATE
  ALTER TABLESPACE                 CREATE OPERATOR CLASS            DROP EVENT TRIGGER               EXECUTE                          VACUUM
  ALTER TEXT SEARCH CONFIGURATION  CREATE OPERATOR FAMILY           DROP EXTENSION                   EXPLAIN                          VALUES
  ALTER TEXT SEARCH DICTIONARY     CREATE POLICY                    DROP FOREIGN DATA WRAPPER        FETCH                            WITH
  ALTER TEXT SEARCH PARSER         CREATE PROCEDURE                 DROP FOREIGN TABLE               GRANT                            
pico=# \?
pico=# \l
                                 List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges   
-----------+----------+----------+------------+------------+-----------------------
 pico      | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
(4 rows)

pico=# \c pico
psql (14.5 (Ubuntu 14.5-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
You are now connected to database "pico" as user "postgres".
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# SELECT flag
pico-# SELECT * FROM flags
pico-# select * from flags;
ERROR:  syntax error at or near "*"
LINE 2: SELECT * FROM flags
               ^
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://cloud.google.com/spanner/docs/psql-commands?hl=es-419#:~:text=psql%20es%20el%20frontend%20de,datos%20de%20dialecto%20de%20PostgreSQL.