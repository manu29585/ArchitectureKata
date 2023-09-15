# O'Reilly Architecture Kata September 2023

This is a team submission for O'Reilly [Architecture Katas 2023](https://learning.oreilly.com/featured/architectural-katas/).

Team Members

- Manohar M
- Sairam Sadanandan
- Somaraj K
- Shreyas Udupi
- Shashwat Bajpai

## Table of Contents

- Introduction - Done
- Business Context
  - Requirements - Done
  - Constraints - Done
  - Risks  - Done
  - Assumptions - Done
- [ArchitectureApproach](#systematic-architecture-design) - Done
  - [Idea](#idea) - Done
  - [Requirements](#requirements)- Done
  - [DomainModel](#domain-model) - Done
  - [Environment](#environment) - Done
  - [NFR](#nfr) - Done
  - [HighLevelArchitecture](#architecture) - Done
  - [KeySubsystems&Design](./KeySubsytems.md) - Done
  - [ADR]
    - [TypeOfArchitecture] - Done
    - [CommunicationProtocol] - Done
    - [DeploymentStrategy] - Done
    - [APIGateway] - Done
    - [UITechnology] - Done
    - [Caching] - Done
    - [Database] - Done
  - [Diagram]
    - [UseCases] - Done
    - [SystemLevelViews] - Covered with high level arc
    - [CICD] - Done
  - [Testability]
    - [TestStrategy](./TestStrategy.md) - Done
    - [TestPyramid](./TestPyramid.md) - Done
  - [CrossCuttingConcerns]
  - [NFRRepresentation] - Covered with high level arc
    - [Logging] - Centralized logging
    - [Auditing]
    - [Monitoring]
      - [AppInsights]
    - [Security]
      - [RateLimiting]
      - [DataIntegrity]
      - [Confidentiality] - How do we do profile protection, Analytics - How can we anonymize the data?

## Target for 13/09

- Business description and context setting
- Sub system interaction with high level choice of technologies/tooling
- High level architecture finalized

## Target for 14/09

- All sub systems High level design
- Testability
- ADR 
  - API Gateway
  - Choice of UI technologies - Xmarin/ts/js - How to make it compatible with Android/iOS/Web?
  - Communication technology(rest/grpc/websocket) for micro service internal communication
  - Choice of DB (AWS Aurora) (Because of less read latency < 20ms>)
  - Choice of caching (Redis/Elasticache)

## Target for 15/09

- NFR handling and associated diagram representation
- Final flow walkthrough
