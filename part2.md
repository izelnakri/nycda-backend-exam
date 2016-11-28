## NYCDA Backend Exam - Part 2

Given that we have a "customer" resource/model in our web server,

### 1 - How would you design the routes of your server based on REST convention? List them with VERB and /route
| HTTP VERB/METHOD | ROUTE               |
| ---------------- | :-------------------|
| GET              | /customers          |
| GET              | /customers/new      |
| POST             | /customers          |
| GET              | /customers/:id      |
| GET              | /customers/:id/edit |
| PUT              | /customers/:id      |
| DELETE           | /customers/:id      |

### 2 - Which routes would require templates, and how would you name the templates? List them with /route and template-name.extension

| HTTP VERB/METHOD | ROUTE               | TEMPLATE             |
| ---------------- | -------------------:| --------------------:|
| GET              | /customers          | /customers/index.hbs |
| GET              | /customers/new      | /customers/new.hbs   |
| GET              | /customers/:id      | /customers/show.hbs  |
| GET              | /customers/:id/edit | /customers/edit.hbs  |

=========

### 3 - What is a database constraint? Name the 3 types of database constraints you have learned.
- foreign key column - points to a primary key in another table
- not null column  - can not be null (empty)
- unique column - has to be unique, not the same value as in another record

### 4 - What is a foreign key? Given that you have a Factory that has many cars and car that belongs to a factory, What would be your foreign key column?

A column in a table that contains the id of a row in another table. If there is a mismatch database wont allow the insertion.

Cars table has factoryId column that refers to the Factories tables. In other words each car has one factory.

### 5 - List all the model lifecycle hooks you have learned from sequelize and explain them briefly if necessary.

These two run when each database action:
- before validate
- after validate

These two run when persisting the model instance for the first time:
- before create
- after create

These two run when updating a persisting model instance each time:
- before update
- after update

These two run when deleting a persisted model instance:
- before destroy
- after destroy

- for example , we can  put a slug for posts if they don't have one, before create  the post.

### 6 - What is the difference between database-level validations and application-level validations?

database-level validation , we put the validation in the database and in the migration files  and when we create the tables. like defining constrains for columns.
application-level validations, we put validate property to do this validation in model part.

### 7 - Why do we use bcrypt. Write down 3 reasons why we use it if you can.

- Bcrypt hashes cannot be decrypted. We store encrypted version in our database
- Hashing algorithm is intentionally slow to prevent brute force cracking.
- You can compare two encrypted hashes to see if they are from the same source

### 8 - What is a flash message?
They are notification messages , to show users that an action was successful or unsuccesfull. They are sourced from the application code, application-level validations or db-level validations and passed down to templates for rendering.

### 9 - What is the difference between minifying and obfuscating JavaScript?


### 10 - What are the 3 reasons that makes Gulp a good choice as an asset build library?

1 - It leverages node streams, follows the node way.
2 - It is intuitive and easy to configure.
3 - There are many packages out there for doing the standard tasks so you dont have to write custom logic.
