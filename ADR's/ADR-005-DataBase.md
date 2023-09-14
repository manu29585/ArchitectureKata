# Title: ADR-005: DataBase
## Date: 2023-09-14
## Status: Accepted

## Context
We need to choose a database for our microservice architecture, which will have 2 million active users per week and a total user base of more than 15 million. Database should be scalable, reliable, and performant.
 
## Decision
Cosidering that information stored in Road Warrior is structured with fixed schema It is decided to use Amazon Aurora Serverless as our database for microservice architecture.
Amazon Aurora Serverless is a fully managed MySQL and PostgreSQL compatible relational database that is designed for scalability, reliability, and performance. It is also a pay-as-you-go service, so we only pay for the resources that we use.

![DB Comparison](DBComparison.png)
## Consequences
It may need to adjust the application architecture to accommodate the pay-as-you-go pricing model.

## Mitigation
Identify areas in Architecture where we can reduce the amount of read and write operations that we perform on the database by implementing caching or batch processing

## Next steps
* Set up an Amazon Aurora Serverless cluster.
* Create a database schema.
* Start migrating our data to Aurora Serverless.
