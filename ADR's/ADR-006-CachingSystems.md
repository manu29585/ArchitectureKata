# Title: ADR-006: Caching System
## Date: 2023-09-14
## Status: Accepted

## Context
We need to choose an in-memory caching system for our microservice architecture, which will have 2 million active users per week and a total user base of more than 15 million. We need a caching system that is fast, scalable, reliable,  easy to use ,high uptime
 
## Decision
We have chosen to use Amazon ElastiCache for Redis Accelerator as our in-memory caching system. Amazon ElastiCache for Redis Accelerator is a fully managed service that makes it easy to deploy, manage, and scale Redis in the cloud.
Amazon ElastiCache for Redis Accelerator is paid services and it has the below advantage over open source
* Ease of use: Amazon ElastiCache for Redis Accelerator is a fully managed service, so you don't need to worry about setting up or managing the infrastructure.
* Scalability: Amazon ElastiCache for Redis Accelerator can scale to meet your needs, even for high-traffic applications.
* Reliability: Amazon ElastiCache for Redis Accelerator is highly reliable and backed by Amazon's commitment to uptime.
Support: Amazon ElastiCache for Redis Accelerator offers 24/7 support from Amazon experts.


## Consequences
Need to pay a monthly subscription fee.

## Mitigation
To mitigate the cost of using Amazon ElastiCache for Redis Accelerator, we will use a managed service such as Amazon ElastiCache for Redis Accelerator. These services can help us to reduce our costs by automatically scaling the cache up and down based on our usage

## Next steps
* Set up an Amazon ElastiCache for Redis Accelerator cluster.
* Configure our microservices to use the cache.
* Monitor the performance of the cache and make adjustments as needed.
