#### Definition of complexity
It is a software system that refers to how difficult it is to understand and verify the  design and its implementation.
this can be dependent on many factors 
1. Size of the system  - Bigger system ? More complex
2. Number of components involved  - More components ? can lead to increased complexity
3. internal structure - how are the above components organised and the way they interact 
4. interdependencies - relationship between components 

### How can we handle **complexity** ? 
To handle complexities certain design patterns are recommended. they are below!

1. Seperate concerns : divide a system into different components or services, such that each component is responsible for a specific function. This reduces complexity by clearly stating what each part needs to handle.
2. Functionality Inside Components : its suggested to have only one functionality within each component or service. this makes components more focused and easier to understand
3. Interactions in connections : create an interaction b/w components using connector as Dr gary suggested like an adapter, we can use API or pubsub.This separates the logic of how components communicate from their internal logic, further reducing complexity
4. Cohesive Components/Services: we need to ensure that each component or service is cohesive, which means it should only perform functionality related to its specific purpose. this makes each component simpler and easy to maintain.
5. Impact of Off-the-Shelf Components: We need to be cautious about using about external or external party usages . like third party libraries or components as they may add complexity.
6. Insulate from Data Format Changes: We need to design components such that they can recover quickly (resilient) to change in data forms . this can be done by abstraction layers as they protect the core functionality from changes in input/output format.

#### Role of design in complexity Management.
----
Design Patterns: At a lower level, recurring problems in code organization led to the develop the design patterns, which are solutions to common design issues. They help in organizing code in a way that reduces complexity.

Architectural Decisions : At the higher level, architectural decisions are important for managing complexity in large systems. This involves choosing how to structure the overall system and how different components will interact.

#### Dependability ---> Trustworthy and Reliable
Dependability refers to set of properties that makes one to rely on system.It includes different elements that help the system work properly, even when things get tough.
1. Reliability : The probability that a system will perform its actual function correctly under specific conditions and within a given time. without failure.
2. Availability : The probability that a system is operational and accessible at a specific moment when needed.
3. Robustness: The ability of a system to handle unexpected conditions at runtime.
4. Fault-tolerant: capability of a system to continue operating smoothly even when some components fail. example k8's pods if one pod fails or dies the deployment soon makes sure the actual vs desire comparison and spins the next pod in action.
5. Survivability: ability of a system to withstand, recognize, recover from, and adapt to threats that may compromise its mission or goal.
6. Safety: assurance that a system will not fail in a way that causes unacceptable consequences, such as loss of life, injury, or significant property damage.


#### Architecture (styles) versus Design (patterns)
refer Design Patterns and Architectural Decisions before proceeding further we discussed them before.
***Key points relating to Architecture***.
1. Partitioning: Involves dividing the software system into distinct modules or components.
2. interactions: Emphasizes the connections and interactions relating to the components . This includes understanding how data flows between parts and how they are communicated.
3. structural properties: responsible with the overall structure and organization of the system. It answers questions like, “How does it all fit together?”
***Architectural styles*** : 
An architectural style defines a particular way of organizing architectural elements (e.g., microservices, layered architecture, etc..). Each style has its own set of principles and guidelines.
***decision making***
Architecting also involves in  making the decisions that affect the entire system from various perspectives (e.g., performance, scalability, maintainability). These decisions always reflect the organization’s goals and standards.

***Key points relating to Design***.
1. granularity: design will work on a more detailed level when compared to architecture. It includes decisions about specific services, components, and how to implement code.
2. design patterns: At the code level, design patterns are established solutions to common programming problems. They provide a way to structure code effectively.
3. cohesion and coupling: our  major focus of design is achieving high cohesion (relating of functionalities within a component) and loose coupling (minimizing dependencies between components). This promotes maintainability and flexibility.
***Collaborative Patterns***  : it involves decision-making as well, but is applied at a much more granular level and often follows collaboration pattern (how components work together to achieve a specific functionality.)

Let's Understand ***architectural styles*** as part of the Assignment:

What is an architectural style ? Architectural styles provide a fundamental schema for organizing the structure of software systems.
They define how components collaborate and interact within a system.
Buschmann highlights that architectural style provide a foundation framework for organizing software systems. what it means is they set the stage for how different components of a system interact and collaborate.

***fundamental structure organization***: it defines how a system is defined at higher level.helps in defining roles and responsibilities of different components and how they fit together within a system.

***Styles of Collaboration***: it outline specific ways that elements of a system work together. includes defining how data and control flow between these components, which is crucial for ensuring the system operates effectively and efficiently.

### Achieving Different Goals
1. Organizing System Elements
2. Adapting to Infrastructure Changes

### Organizing System Elements  (Layered, Pipe-Filter)
Some styles focus on how to effectively organize different parts of the system.


***Layered Architecture*** 
Description: This style organizes the system into layers, each with a distinct role. For example, you might have a presentation layer (user interface), a business logic layer, and a data access layer.
Goal: This separation of concerns makes it easier to manage complexity, enhance maintainability, and promote reuse.


***Pipe-Filter Architecture***
Description: in this style, the system is composed of a series of processing elements (filters) connected by data streams (pipes). Each filter processes the data and passes it to the next one.
Goal: this approach helps in promoting modularity and allows for easy addition or modification of processing steps without affecting the entire system

### Adapting to Infrastructure Changes 
Some styles are designed to make changes in the underlying infrastructure without requiring major modifications to the system itself.
***Microkernel Architecture***
Description: This style uses a minimal core system (the microkernel) that provides essential services, while additional features and functionalities can be added as separate modules or plugins.
Goal: This allows the system to adapt easily to new requirements or changes in technology (like database changes or adding aditonal feature) without restructuring the entire application.

### Key Components in Architectural styles:
1. Elements (Automobile Architecture): Wheels, Engines, Mufflers: These are essential parts of a vehicle that contribute to its overall functionality.
2. Elements (Software Equivalent)
   + Components: The modules or services that perform specific functions (e.g., a user interface module). 
   + Connectors: The mechanisms for communication between components (e.g., APIs, message queues).
   + Services: Specific functionalities offered by the components (e.g., authentication service).
3. Types (Automobile Types) : Cars, Trucks , Different categories of vehicles that serve various purposes.
4. Types (Software Equivalent Types) : Gaming Applications  , Email Clients: Distinct categories of software that have unique functional requirements.
5. Styles: (Automobile Styles) : Sedan , XUV , flatbed.
6. Styles (Software Equivalent) : Black board ,Peer to peer 
    + Black board : Blackboard architectural style is designed for applications that require collaboration among various components to solve complex problems. It uses a shared data structure  that allows different components to contribute to a solution.
    + peer to peer : Peer-to-Peer (P2P) architectural style is characterized by a decentralized approach where each node (or peer) in the network acts as both a client and a server. Peers share resources directly without relying on a central server.
7. Rules and Regulations (Automobile R&R): fuel type, structural requirements ,we can call them as standard structures how vehicles can be built and operated.
8. Rules and Regulations (Software R&R):
    + Interfaces: Define how components interact and communicate, ensuring they can work together smoothly.
    + Architectural Policies: Guidelines that govern system behavior and design (e.g., security protocols, performance criteria)