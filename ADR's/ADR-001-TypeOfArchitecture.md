# Title: ADR-001: Type of Architecture

## Date: 2023-09-13

## Status: Accepted

## Context

The purpose of this ADR is to document the decision to use of microservices and event-based architecture for "The Road Warrior" system.

## Decision

The decision to use a microservices and event-based architecture architecture was made after careful consideration of the following factors:

### Microservices

* The Road Warrior Application is expected to be deployed in the cloud, and a microservices architecture will make it easier to scale the system to meet demand.
* The Road Warrior Application is expected to be large and complex (Handling 2 million users in parallel), and a microservices architecture will allow us to break it down into smaller, more manageable components.
* The Road Warrior Application is expected to evolve over time, and a microservices architecture will make it easier to add new features and functionality.

### Event Based

* The Road Warrior Application is expected to be event-driven, and an event driven architecture will make it easier to implement this requirement.
* The Road Warrior Application is expected to be loosely coupled, and an event driven architecture will make it easier to achieve this.
* The Road Warrior Application is expected to be scalable, and an event driven architecture will make it easier to scale the system.

## Consequences

The consequences of using a microservices architecture include:

* The system will be more complex to design and implement.
* The system will require more monitoring and management.
* The system will be more difficult to test and debug.

The consequences of using an event driven architecture include:

* The system will be more complex to design and implement.
* The system will require more monitoring and management.
* The system will be more difficult to test and debug.

## Mitigation Strategies

The following mitigation strategies will be used to address the challenges of using a microservices architecture:

* We will use a well-defined microservices architecture framework to guide the design and implementation of the system.
* We will use a service mesh to manage communication between microservices.
* We will use a continuous integration and continuous delivery (CI/CD) pipeline to automate the deployment and testing of microservices.

The following mitigation strategies will be used to address the challenges of using an event driven architecture:

* We will use a well-defined event driven architecture framework (like RabbitMQ) to guide the design and implementation of The Road Warrior Application..
* We will use a message broker to manage communication between components of The Road Warrior Application..
* We will use a continuous integration and continuous delivery (CI/CD) pipeline to automate the deployment and testing of The Road Warrior Application.

## Next Steps

The next steps are to:

* Complete the design of the microservices and event driven architecture.
* Implement the microservices and event driven architecture.
* Deploy the microservices and event driven architecture to the cloud.
