# User and Email Microservices

## Description

This is a microservices project developed in Java with Spring Boot for user management and the sending of welcome emails. The User and Email microservices operate independently but communicate asynchronously through RabbitMQ to achieve a high level of scalability and maintainability.

## Technologies Used

- Java 17
- Maven as a dependency manager
- Spring Boot
- Spring Web
- Spring Data JPA
- Spring Validation
- Spring AMQP
- Spring Mail
- PostgreSQL
- RabbitMQ
- CloudAMQP
- SMTP Gmail

## Features

The User and Email microservices offer the following features:

### User Microservice
- Registration of new users on the platform.
- User management in the database.
- Sending messages to RabbitMQ to notify the Email microservice.

### Email Microservice
- Receiving messages from RabbitMQ.
- Sending welcome emails to new users.
- Storage of sent emails in the database.

## Asynchronous Communication

Asynchronous communication between the microservices is accomplished through RabbitMQ, which acts as a broker to forward messages from one service to another. The User microservice acts as a producer, sending messages to RabbitMQ, while the Email microservice acts as a consumer, receiving and processing the messages.

## How to Run

1. Clone the repository.
   ```sh
   git clone https://github.com/GustavoSilvalgs/microservices-user-email.git
   ```
2. Configure the properties in the `application.yml` file for each microservice.
3. Run both microservices.
4. Ensure that RabbitMQ is running to enable asynchronous communication.

## Author

Gustavo Silva (https://github.com/GustavoSilvalgs)

## License
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/GustavoSilvalgs/microservices-user-email/blob/main/LICENSE)
