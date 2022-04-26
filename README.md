![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=OPEN%20PROJECT&color=GREEN&style=for-the-badge)

# About
Project that demonstrates the creation of an online course platform using great technologies available in the market today. The entire project was based on a microservices architecture.

# Technologies

## Infra
- Docker Compose
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

## Final application screens
![1](https://user-images.githubusercontent.com/6998981/165199200-12a08952-b35c-4668-ac7f-d4e6db5b205c.jpg)
![2](https://user-images.githubusercontent.com/6998981/165199211-d8222cc3-11d9-41dc-bfd9-a0fe4133b879.jpg)
![3](https://user-images.githubusercontent.com/6998981/165199227-6a64acde-841c-4a70-97fa-e80eeb7d371a.jpg)
![9](https://user-images.githubusercontent.com/6998981/165199269-5c78ad68-0c96-456b-96bc-5c6ede004897.jpg)
![5](https://user-images.githubusercontent.com/6998981/165199245-d37d966a-5f78-4597-899b-8c51b3b9c41e.jpg)
![6](https://user-images.githubusercontent.com/6998981/165199254-88ad60fa-8546-42dd-bfa4-86dadbaf8de1.jpg)
![8](https://user-images.githubusercontent.com/6998981/165199262-9c7c7e08-0be8-4a32-ad7f-4fb857065541.jpg)
![4](https://user-images.githubusercontent.com/6998981/165199238-9b0e99a4-1c66-44cd-b7d5-a05f2e43a388.jpg)

## Backend features

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

```bash
docker-compose up
```

### Step 3
#### Classroom service
Create a .env file with parameters bellow:

```env
AUTH0_AUDIENCE=/** Register on Auth0 and get the parameter **/
AUTH0_DOMAIN=/** Register on Auth0 and get the parameter **/

DATABASE_URL="postgresql://docker:docker@localhost:--port(default 5432)/classroom?schema=public"
```

#### Purchase service
Create a .env file with parameters bellow:

```env
AUTH0_AUDIENCE=/** Register on Auth0 and get the parameter **/
AUTH0_DOMAIN=/** Register on Auth0 and get the parameter **/

DATABASE_URL="postgresql://docker:docker@localhost:--port(default 5432)/purchases?schema=public"


KAFKA_BROKERS=localhost:--port(default 29092)
```

### Step 4
Run the following commands in the respective directories of the created services (backend) "classroom" and "purchases"

```bash
//Installing dependencies
npm install

//Executing migrations on Prisma (database)
npx prisma migrate dev

//Run
npm run start:dev
```

### Step 5
Run the Gateway

```bash
//Installing dependencies
npm install

//Run
npm run start:dev
```

### Step 6
Run the bellow commands to up the frontend application

```bash
// Installing dependencies
npm install or yarn

// Run
npm run dev or yarn dev
```

### ⚠️ Help

If message "Cannot found module" appears, you have to run the command bellow

```bash
npm link --name-module
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Thanks to
[Rocketseat](https://github.com/Rocketseat) :rocket::purple_heart:
