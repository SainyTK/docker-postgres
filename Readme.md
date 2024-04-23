# Docker compose template for Postgres Database
This repository contains the template files and folders to get started with Postgres Database setup and important commands.

## Structures
1. `docker-compose.yml`: The main file to contain main commands to pull in Postgres to Docker.
2. `backup`: This is the place where you can dump .sql files whether to export or import data.
3. `data`: This is the folder mapped to the docker volume used as a database storage.

## Commands 
1. Run database <br/>
`docker compose up -d --wait`
2. Shell to database <br/>
`docker compose exec db /bin/bash`
3. Login to postgresql db <br/>
On the db shell: `psql -U postgres`
4. List databases <br/>
On the psql shell: `\list`
4. Create a new database <br/>
On the psql shell: `CREATE DATABASE "DBNAME"`. Replace "DBNAME" with your database name.
5. Seed data with .sql file to db <br/>
On the host terminal: `cat "path-to-sql-file" | docker compose exec -T db psql -U postgres -d "db_name"`. Replace "path-to-sql-file" to the relative path to sql file and "db-name" to the database name.
6. Seed data with .dump file to db <br/>
On the host terminal: `cat "path-to-sql-file" | docker compose exec -T db pg_restore -U postgres -d "db_name"`. Replace "path-to-sql-file" to the relative path to sql file and "db-name" to the database name.
7. List data in a db:

7. Exit psql shell <br/>
On the psql shell: `\q`
8. Exit db docker shell: <br/>
On the db shell: `exit`

## Notes
1. Username is `postgres`

## TODO
- Complete the command lists (import data, list tables, show data)