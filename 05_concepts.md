# Concepts

## Performance Optimization Strategies

### Event queueing

In case the active user load is substantial, and trip notifications become a bottle neck for Dashboard Coordinator to handle. 
A message queuing mechanism is introduced. Standard messge queing solutions like RabbitMQ or Kafka would be used within the Service boundaries.

The same solution could be applied to other containers as well to do load balancing.

### Read replicas

On recieving trip details; services like Trip Organizer shall also cache the updates to a in-memory read replica.
This read replica will be used to improve the user experience, for e.g. during the usecases when trip details need to be updated.

![High level architecture](.media/Message-Queueing-In-Dashboard-Coordinator.png)

## Build and security by design

### CI-CD pipeline design for automated tests and deployment

![Build Pipeline](.media/road-warriors-build.drawio.png)

### Security as a defacto standard

![Security in Build Pipeline](.media/security-build-pipeline.drawio.png)

### Caching

[Caching](caching.md)

### Test Strategy

[TestStrategy](TestStrategy.md)

#### Test Pyramid

[TestPyramid](TestPyramid.md)

