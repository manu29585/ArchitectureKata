# Title: ADR-007: Deployment strategy

## Date: 2023-09-14

## Status: Accepted

## Context

We need to deploy our microservice application to production which includes multiple microservices, API gateway and DataBase on cloud

## Decision

After careful consideration, we have decided to deploy our microservices-based application on a container orchestration platform, specifically using Kubernetes.

We will use the following deployment pattern:

* Microservice application: Each microservice will be deployed as a separate Kubernetes deployment
* API gateway: The API gateway will be deployed as a single Kubernetes deployment
* Redis DB: The Redis DB will be deployed as a single Kubernetes deployment

## Consequences

* Operational Complexity: Managing a Kubernetes cluster can be complex and may require dedicated resources
* Infrastructure Costs: Running Kubernetes clusters and managing infrastructure can add operational costs

## Mitigation

* We will use a deployment pipeline to automate the deployment process. This will help us to reduce the risk of errors
* We will use a service mesh to provide communication between our services. This will help us to make our services more resilient
* We will use a load balancer to distribute traffic across our services. This will help us to ensure that our services are available to users even if one service is overloaded

## Next steps

* Implement the deployment pipeline
* Configure the service mesh
* Configure the load balancer
* Deploy the microservice application, API gateway, and Redis DB to   production on Kubernetes
