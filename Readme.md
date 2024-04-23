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
On the psql shell: `CREATE DATABASE "DBNAME">`. Replace "DBNAME" with your database name.
5. Exit psql shell <br/>
On the psql shell: `\q`
6. Exit db docker shell: <br/>
On the db shell: `exit`

## Notes
1. Username is `postgres`