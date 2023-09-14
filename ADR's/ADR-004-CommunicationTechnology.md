# Title: ADR-004: Communication Technology
## Date: 2023-09-14
## Status: Accepted

## Context
We need to choose communication technologies for our microservices to communicate with each other. We want to choose technologies that are scalable, reliable, and easy to use.
 
## Decision
We have decided to use gRPC as our communication technology for microservices. gRPC is a high-performance, open-source RPC framework that is built on top of HTTP/2.

![Communication Technology Comparison](CommunicationTechnologyComparison.png)
## Consequences
The main consequence are 
* Learn a new technology. 
* gRPC can be more complex to setup and use than other communication technologies.
  However, gRPC offers a number of advantages over other technologies, such as its performance and reliability

## Mitigation
Complexity of gRPC can be addressed by
* Using a gRPC framework such as grpc-web or grpc-gateway to make it easier to use gRPC from different programming languages and platforms.
* Using a gRPC observability tool such as OpenCensus or Jaeger to monitor and troubleshoot gRPC traffic
## Next steps
* Ramp up on gRPC
* Set up a development environment for gRPC 
* Prototype using gRPC to communicate between  microservices
