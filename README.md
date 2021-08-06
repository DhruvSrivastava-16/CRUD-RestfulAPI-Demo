# Demo of the RESTful API I made for the hostel management system. 

#### Since the real application is the property of Mahindra University, I can't share it publically 

Implementing CRUD operations on PostgreSQL database on a Node.js application with a server made using Express.js



## Database

```bash
brew install postgresql
brew services start postgresql
psql postgres
```

```sql
CREATE ROLE demo WITH LOGIN PASSWORD '123456';
ALTER ROLE demo CREATEDB;
CREATE DATABASE api;
GRANT ALL PRIVILEGES ON DATABASE api TO demo;
```

```bash
psql -d api -U me
```

```sql
CREATE TABLE users (
  ID SERIAL PRIMARY KEY,
  name VARCHAR(30),
  email VARCHAR(30),
  hostel VARCHAR(30),
 Room VARCHAR(30),
);

INSERT INTO users (name, email)
  VALUES ('Lawrence', 'abcdef@gmail.com','Hostel A','14C'), ('Rohan', 'opqwe@gmail.com','Hostel B','12D'),('Tony', 'zxcvb@gmail.com','Hostel C','9A');
```



## Commands

- GET: `curl http://localhost:3000/users`
- POST: `curl --data "name=Jerry&email=jerry@example.com" http://localhost:3000/users`
- PUT: `curl -X PUT -d "name=George" -d "email=george@example.com" http://localhost:3000/users/1`
- DELETE: `curl -X "DELETE" http://localhost:3000/users/1`

## Author

- [Dhruv Srivastava](https://dhruvsri123.github.io/)

