## Architecture overview

**Software Architecture** is the fundamental design of the software system. It defines what **elements** are included in the system, what **function** each element has, how each element **related** to another. In plain text, it is the big picture (overall structure) of the whole system.

Some considerations that the architect will consider while planning the structure of the system:

- What will the system be used for?
- Who will be using the system?
- What qualities matter most to them?
- Where will the system run?

**Why do we need software architecture?**

- Having a clear design of the system as starting point helps to provide **basis for developers to follow**, each developer will then know that **needs** to be implemented and how thing relate to meet the desired needs efficiently.
- **Higher productivity** for your software team, as a well-defined structure helps to coordinate work, implement individual features, or guide discussions on potential issues.
- A clear architecture will help to achieve **quality** in your software, with a well-design structure using principles like separation of concerns, the system will be easier to maintain and reuse.

**Stakeholders** are the people who have an interest in the software system or people who will using the system. So how **software architecture** help people like developers, end users, project managers and clients?.

- **Software Developers** ⇒ Software architecture helps developers create and evolve software by providing strong direction and organization on what needs to be done or built.
- **Project Managers** ⇒ Software architecture provides useful information to help them identify possible risks, manage the project successfully and understand task dependencies.
- **Clients** ⇒ Clients make important decision about the system like **funding**, if there a good architecture to understand what they are paying for and their needs are met.
- **End Users** ⇒ They care that if the app "works well" for them

### Kruchten's 4 + 1 Model View (4 plus 1 view model)

There are several considerations to capture the complete the behavior of the software system. 

- **Logical View** ⇒ One consideration is the **functionality** of the software that satisfy what a client wants, which call **Logical View** which focuses on the functionality of the system and the objects found within it.
- **Process View ⇒** Another consideration is how the software executes? including characteristics like the efficiency of the system, performance and scalability called **Process View** which focus in the process of implementing the Logical View.
- **Development View ⇒** The Implementation, the structure and its the programming languages of your software can considered as **Development View.**
- **Physical View** ⇒ The physical components that are needed to deploy like one server for database and other host for your web clients, **Physical view** plan how these elements interact to deploy the system correctly.

Without knowing what the system achieve for its users, it would be **difficult** to detail these views.

These views together are from **Kruchten's 4 + 1 View Model**, that do follow these 4 views and perspectives to create software architecture instead of one single perspective of the system.

- **Logical View** ⇒ focuses on achieving the **functional requirements** of a system and the services that should be provided to end users. You can create **UML Class Diagram** that illustrates the objects in the logical view and also describe database schemes.
- **Process View ⇒** focuses on achieving the **Non-functional requirements** to specify the qualities for the system like performance and availability. **UML Sequence Diagram** help for illustrating the methods and how they are executed and its order, **UML Activity Diagram** can illustrate the processes or activities for a system
- **Development View ⇒** focuses of details of software development and considers elements like programming languages, libraries and tools, also beside code it handles project management details like scheduling, budgets and work assignments.
- **Physical View** ⇒ focuses on handles logical, process and development views in different nodes or hardware for running the system, a UML Deployment Diagram express how the pieces of a system are deployed into hardware.

No all software architectures need to be documented using 4 + 1 view model, if any of the view is useless so can be ignored.

### UML Component Diagram

Component diagram is high-level structure used to visualize how a system's pieces interact and what relationships they have among them. Focus on the components of a system and interactions between them not their methods and implementations.

This diagram is concerned with the components of a system. Which components are defined as independent encapsulated units within a system, each component provides and interface for other components to interact with it including third-party libraries.

**Diagram Components Relationship**

- **Ball Connector**: displays a provided interface

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/component-diagram-1.png" width="100" hight="100"/>
</p>

- **Socket Connector**: displays a required interface (component expects a interface)

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/component-diagram-2.png" width="100" hight="100"/>
</p>

- **Relationship** shows that the component provided interface matches another component's required interface

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/component-diagram-3.png" width="200" hight="200"/>
</p>

**Steps to build a Component Diagram**

- Define the **main objects** used in the system
- Define the **relevant libraries** you need for your system
- Define the **relationships** between these components

**Example of a component diagram for a video game system.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/component-diagram-4.png" width="500" hight="500"/>
</p>
