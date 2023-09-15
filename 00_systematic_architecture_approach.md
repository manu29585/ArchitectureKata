# Systematic software architecture

## Systematic Architecture Design

For this architecture challenge we have followed the systematic architecture design (SAD) technique. ![SAD](.media/SAD.png)
The SAD is broadly classified into 2 categories:

1) Problem Space
2) Solution Space

### Problem Space

The major components involved in the problem space are:

- Idea : In this phase we define the the customer need/wish.

- Requirement & User Story: The is the phase we perform the requirement elicitation and document the requirement as for of user stories.

- Domain Model : In this phase we use a common language to define the entities, problem domain and the interaction between them. The domain model will also include the constraints and boundaries

- NFR : In this phase we define all the non-functional requirements such as quality scenarios, quality tree, architectural drivers.

- Use Cases: In this phase we define the interaction between the components.  

**NOTE**: The Product backlog in the SAD diagram is added for the sake of completeness. 

## Architecture

- In order to chose the architecture, we followed the [Systematic Architecture Design](#systematic-architecture-design).
- In this approach, we first started with the problem domain and then moved toward a solution domain.
- In the solution domain, we worked on three different set of architectures.

1) Draft Architecture

- Draft architecture is a result of problem space.
- Independent of Technology & interfaces.

2) Reference Architecture

- This includes technical details.
- Uses the existing reference templates. For example, any other existing architecture which might have similar use cases.

3) Baseline Architecture

- Contains NFR solutions
- This architecture contains the architecture for existing environment.

- After going through this iterative process we decided to go ahead with the hybrid architecture i.e. Microservices & Event Driven
![Architecture](.media/ArchitectureStyleSheet.png).

- For deciding the underlying architectures (i.e. Microservices and Event based) we have created an ![ADR](adr's/ADR-001-TypeOfArchitecture.md)
