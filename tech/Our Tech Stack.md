# Full Port DEV's Tech Stack

## Philosophy
- reusability
  - never repeat yourself,
- SaaS
  - we rely heavily on SaaS in order to reduce over

## Frontend: Svelte
Svelte is FullPortDEV's bread and butter - no other framework allows us to build such robust, performant and extendible frontend code

- an estimated 40% less code means half the code to read, write, delete and maintain. 

- hiring. 
  - developers frustrated by the React ecosystem 
  - keen developers looking to push the bounds by using cutting edge technology
  - hightened developer experience
  - reduced hours spent

- However, if the project calls for it and the client specifically requests it - we can and will build with React


## Backend: Python FastAPI
- FastAPI 
- FastAPI uses pydantic for data validation, using our pydantic -> javascript validator we have one source of truth for data validation.
  - enables us to

## Backend: Express
- lightweight
- validators written in Express are natively able to be reused

## Databases
### Database: Redis
- we use redis as a primary database for a lot of our problems
- most problems break down into simple CREATE READ UPDATE DELETE (CRUD) operations, as such a document database is more than sufficient for 90% of problems
- therefore, we optimize for read and write speed - something Redis is incredible for


### Database: MongoDB
- anything that requires more complex queries
- 

## Deployment
- we leverage SaaS platforms
- and hosted versions of databases
  - MongoDB
  - Redis


## Authentication
- passport.js
  - the one thing we don't rely upon is Authentication
  - we implement our own Authentication system using state of the art framework, Passport.js
  - the advantage of using this is that we can easily and seamlessly utilize your own oauth provider
    - example. OSPE
  - given a 