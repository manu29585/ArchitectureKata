# O'Reilly Architecture Kata September 2023

This is a team submission for O'Reilly [Architecture Katas 2023](https://learning.oreilly.com/featured/architectural-katas/).

Team Members

- Manohar M
- Sairam Sadanandan
- Somaraj K
- Shreyas Udupi
- Shashwat Bajpai

## Table of Contents

- Introduction
- Business Context
  - Requirements  
  - Constraints
  - Risks  
  - Assumptions
- [ArchitectureApproach](#systematic-architecture-design)
  - [Idea](#idea)
  - [Requirements](#requirements)
  - [DomainModel](#domain-model)
  - [Environment](#environment)
  - [NFR](#nfr)
  - [HighLevelArchitecture]
  - [KeySubsystems&Design]  
  - [ADR]
    - [TypeOfArchitecture]
    - [CommunicationProtocol]
    - [DeploymentStrategy]
    - [Scalability]
  - [Diagram]
    - [UserJourney]
    - [SequenceDiagram]
    - [DeploymentView]
    - [WireFrames***]
    - [SystemLevelViews]
    - [CICD]
  - [Testability]
    - [TestStrategy]
  - [CrossCuttingConcerns]
    - [Logging]
    - [Auditing]
    - [Monitoring]
      - [AppInsights]
    - [Security]
      - [RateLimiting]
      - [DataIntegrity]
      - [Confidentiality]

## Target for 13/09

- Business description and context setting
- Sub system interaction with high level choice of technologies/tooling
- High level architecture finalized

## Target for 14/09

- All sub systems High level design
- Testability
- ADR

## Target for 15/09

- NFR handling and associated diagram representation
- Final flow walkthrough

## Systematic Architecture Design

For this architecture challenge we have followed the systematic architecture design (SAD) technique. ![SAD](.media/SAD.png)
The SAD is broadly categorized into 2 categories:

1) Problem Space
2) Solution Space

### Problem Space

The major components involved in the problem space are:

- Idea : In this phase we define the the customer need/wish.

- Requirement & User Story: The is the phase we perform the requirement elicitation and document the requirement as for of user stories.

- Domain Model : In this phase we use a common language to define the entities, problem domain and the interaction between them. The domain model will also include the constraints and boundaries

- Environments: In this phase we define the environment which impact the design such as Existing Systems, Budget, Timelines etc.

- NFR : In this phase we define all the non-functional requirements such as quality scenarios, quality tree, architectural drivers.

- Use Cases: In this phase we define the interaction between the components.  

## Idea

"The Road Warrior" is an online trip management company which allows travelers to see all the of their existing reservations organized by the trip.

## Requirements

The requirements are defined here [Requirements](Requirements.md)

## Domain Model

- Entities: ![Entities](.media/Entities.png)

- High Level System Overview: ![SystemOverview](.media/HighLevelSystemOverview.png)

- System Domain Model: ![SystemDomainModel](.media/DomainModel.png)

- User Interaction and Use Cases: ![UserInteractionAndUseCases](.media/UserInteractionAndUseCases.png)

## Environment

## NFR

| S. No  | Characteristics | Status | Rationale |
| ----------- | -----------| ----------- | ----------- |
| 1) | Scalability |  [x] | The system needs to support multiple users from across the globe. In order to achieve this we should be able to scale our systems (components) horizontally. |
| 2) | Performance |  [x] | The system needs to support multiple users which means there will be high traffic and some of the scenarios (like gate change, cancellation) are time critical. In order to achieve this we should enforce/ define some architecture functions. |
| 3) | Availability |  [x] | The system needs to be available at all times (as the max downtime for the system is just 5 mins). |
| 4) | Usability |  [x] | As the system should have rich UI for the dashboard/summary report we should make sure that we have arch functions defined for usability. |
| 5) | Upgradeability |  [x] | We should be able to update and upgrade the system with additional feature. |
| 6) | Extensibility |  [x] | As the system might have multi vendor, multi service support, we need to make sure that there is no vendor lock-in and the system is easily extensible. |
| 7) | Security |  [x] | As this system stores user information we need to define architecture functions to handle security. |

Other topics to consider

Cost: Since we are talking about having multiple services and these services will be deployed across the continents. The cost is something we need to keep in mind.  
Configurable:
Confidentiality:
Integrity:
Authentication
