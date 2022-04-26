# About
Project that demonstrates the creation of an online course platform using great technologies available in the market today. The entire project was based on a microservices architecture.

# Tecnologias utilizadas

## Infra
- Docker e Docker Compose
- PostgreSQL
- Zookeeper
- Apache Kafka
- Kafka-ui

## Backend (classroom and purchases)
- Typescript
- NestJS
- Prisma
- Auth0
- Apollo e Apollo Federation
- GraphQL
- Streaming with Apache Kakfa
- esLint e Prettier

## Gateway
- Typescript
- Apollo gateway
- GraphQl

## Frontend
- Next.js
- GraphQl
- Apollo Client (GraphQL)
- Auth0
- Codegen
- Tailwindcss
- Headlessui
- esLint

## Funcionalidades

### Purchasing service (purchases)

- [Admin] Product Registration
- [Admin] Product listing

- [Auth] Shopping List

- [Public] Purchase a product
- [Public] List products available for purchase

### Classroom service

- [Admin] List enrollments
- [Admin] List students
- [Admin] List courses
- [Admin] Register courses

- [Auth] List courses I have access to
- [Auth] Access course content

----------------------------------------------------------------
# How to install

### Step 1
Make a clone of the project.

### Step 2
Run docker-compose in the root directory to assemble the entire project infrastructure.
docker-compose up

### Step 3
#### Classroom service
Create a .env file with parameters bellow:

AUTH0_AUDIENCE=/** Register on Auth0 and get the parameter **/
AUTH0_DOMAIN=/** Register on Auth0 and get the parameter **/

DATABASE_URL="postgresql://docker:docker@localhost:--port(default 5432)/classroom?schema=public"

#### Purchase service
Create a .env file with parameters bellow:

AUTH0_AUDIENCE=/** Register on Auth0 and get the parameter **/
AUTH0_DOMAIN=/** Register on Auth0 and get the parameter **/

DATABASE_URL="postgresql://docker:docker@localhost:--port(default 5432)/purchases?schema=public"


KAFKA_BROKERS=localhost:--port(default 29092)
### Step 4
Run the following commands in the respective directories of the created services (backend) "classroom" and "purchases"

//Installing dependencies
npm install

//Executing migrations on Prisma (database)
npx prisma migrate dev

//Run
npm run start:dev

### Step 5
Run the Gateway

//Installing dependencies
npm install

//Run
npm run start:dev

### Step 6
Run the bellow commands to up the frontend application

// Installing dependencies
npm install or yarn

// Run
npm run dev or yarn dev

### Help

If message "Cannot found module" appears, you have to run the command bellow

npm link --name-module
