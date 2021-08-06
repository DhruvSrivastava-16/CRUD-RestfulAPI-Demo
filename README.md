# Demo of the RESTful API I made for the hostel management system. 

#### Since the real application is  property of Mahindra University, I couldn't share the actual code files

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



## Author

- [Dhruv Srivastava](https://www.dhruvsri123.github.io)

