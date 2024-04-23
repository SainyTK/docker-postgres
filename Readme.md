## Commands 
1. Run database <br/>
`docker compose up -d --wait`
2. Shell to database <br/>
`docker compose exec db`
3. List databases <br/>
On the db shell: `\list`
4. Create a new database <br/>
On the db shell: `CREATE DATABASE "DBNAME">`. Replace "DBNAME" with your database name.
5. Exit shell
On the db shell: `exit`

## Notes
1. Username is `postgres`