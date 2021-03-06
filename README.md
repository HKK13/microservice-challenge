## Description

Applications in this repo is not meant for production. 
Also be aware that this repo solves imaginary scalability issues and is tightly coupled.

## Repo Content

This repo contains 4 dockerized microservices:

-  API: API is the entry point of this distributed system. It's main duty is to route requests to corresponding services and return the response to the requesting user. This service will also be the last place where authentication and input validation is handled.

- Badge: Badge system is to handle all requests about badges. (Get, Create, Update, Delete). Badge assigning to a user is out of the scope of this microservice.

-  User: User service is the place where all operations about the user is handled. Badge assigning job is also the job of this service.

- Crypto: Crypto service is where passwords are hashed, compared and salts are generated.

- Logger: Logger service logs the movements of the user scrolls, clicks etc.

Additional Containers:
For easier deployment docker containers are used. Additional containers exist to address rabbitmq, mongo and nginx dependencies.

# Usage:

First Need to build Frontend.
- cd into frontend
- npm install --dev-dependencies
- npm run build

Finally, gently type
- docker-compose build
- docker-compose up

# What Is NOT Done:
- Friend invitations are not available.
