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

Not all software architectures need to be documented using 4 + 1 view model, if any of the view is useless so can be ignored.

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

### UML Package Diagram

A **package** groups together elements (data, classes, functionality) of your software that are related. It defines as a **Namespace** for the elements it contains.

Packages diagram show packages and the dependencies between them to organize your completed system into packages of related elements.

**Package Diagram components**

- **Tabbed folder** (if the package don't have any elements, package name writes in the center of folder)

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/package-diagram-1.png" width="400" hight="400"/>
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/package-diagram-2.png" width="400" hight="400"/>
</p>

- **Importing** and **Merging** other packages into package. Dependencies like `<import>` = public import, `<access>` = private import ⇒ mean one package requires help from functions of other package. `<merge>` = merging two packages into single package. `<uses>` = the package need the full implementation of another package

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/package-diagram-3.png" width="400" hight="400"/>
</p>

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/package-diagram-4.png" width="400" hight="400"/>
</p>

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/package-diagram-5.png" width="400" hight="400"/>
</p>

**Example of UML Package diagram**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/package-diagram-6.png" width="600" hight="600"/>
</p>

### UML Deployment Diagram

Software release involves separate libraries, an executable, an installer, configuration files and other different pieces. Once the environment of all pieces are sit, you would use UML Deployment Diagram to visualize these deployment details for a software system.

UML Deployment Diagram deal with Artifacts. **Artifact** which are a physical result of the development process, For example of video game would be an executable to run the game, an installer, audio libraries and multimedia assets

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/deployment-diagram-2.png" width="200" hight="200"/>
</p>

Two types of deployment diagram

- **Specific Level Diagram**

    Which gives an overview of artifacts and deployment targets without referencing details like machine names. It focuses on a general overview of your deployment.

- **Instance Level Diagram**

    Is much more specific diagram, which can map a an artifact to deployment target. It can identify machines and hardware devices. This approach is used to highlight the differences in deployments amount development, staging and release builds.

**UML Deployment diagram components**

- **Node**: is deployment target that contains artifacts for execution, its the hardware `<<device>>`.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/deployment-diagram-2.png" width="200" hight="200"/>
</p>

- **Relationship between deployment targets**, this relationship between nodes mean that there are a communication path (software or protocol) between them.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/deployment-diagram-3.png" width="300" hight="300"/>
</p>

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/deployment-diagram-4.png" width="400" hight="400"/>
</p>

- `<<manifests>>` relationship between artifacts and which component complied and produce it. Which Player.Class is the encapsulated unit that contains all of the functionality of a player.


<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/deployment-diagram-5.png" width="300" hight="300"/>
</p>

**Example of UML Deployment diagram**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/deployment-diagram-6.png" width="600" hight="600"/>
</p>

Deployment Diagram gives a high level look at the **artifacts**, **libraries**, **main components, machines and devices** that your application needs to run.

### UML Activity Diagram

In this diagram you represent the control flow from one activity to another in a software system, activities is an actions that when completed cause another action to start/execute. For example these action can edit objects or create new objects to drive your application forward. The purpose of this diagram is to capture the dynamic behavior of the system.

**To create Activity Diagram:**

- Identify the activities (actions) performed by the system.
- Identify the conditions of these activities.

**UML Activity Diagram Components**

- **Start and End** nodes must begin (initialize) and end (final) your diagram with them.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/activity-diagram-1.png" width="200" hight="200"/>
</p>

- Intermediate activities that identify to change the application state before ends.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/activity-diagram-2.png" width="200" hight="200"/>
</p>

- Decision node that had the condition to determine which outcomes as the next activity.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/activity-diagram-3.png" width="400" hight="400"/>
</p>

**Example of UML Activity Diagram of video game**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/activity-diagram-4.png" width="600" hight="600"/>
</p>

Also Activity diagrams allow the mapping of activities that happen in parallel and join in single flow after ended. Like if a level ends in a video game, the soundtrack flow will end at the same time as the play flow.

## Language-based Systems

Programming paradigm of the language will affect the architectural system of the system, Each programming paradigm has its own constructs, principles, design patterns, and their use to shape the system you create.

One of these styles of language-based system is **Object-Oriented Architectural Style** which results from the **object-oriented programming paradigm** and use object-oriented approach in the development.

### Object-Oriented Architectural Style

object-oriented principles were explored:

- **Abstraction** that simplify a concept by ignoring unimportant details.
- **Encapsulation** that bundles data and functions into a self-contained object, so other objects can interact with it through an exposed interface.
- **Decomposition** which allows you to break up a whole problem into smaller, distinct parts.
- **Generalization** that allows you to factor out conceptual commonalities.

object-oriented Design Patterns were explored:

- **Creational patterns** that guide the creation of new objects.
- **Structural patterns** that describe the relationships between.
- **Behavioral patterns** that focus on how objects perform work individually or as a group to accomplish something.

These elements together will lead to an object-oriented architectural style for the system. This style focused on the data called **Abstract Data Types** which can be represented as a **class** the define to organize data attributes in a meaningful way along with their associated **methods.**

Object-oriented refers to a system composed of objects where each object is an instance of a class (the type of object is its class), objects interact with each other though the use of their methods. object-oriented programming paradigm allows inheritance, which mean one class can be extension for another class. The classes within the system will determine the overall structure of the system.

### Main Program and Subroutine Architectural Style

Main Program and Subroutine Architectural Style follows from **the procedural programming paradigm**, also C programming language follows this paradigm. This style focused on **functions**, when try to model your system you break up the overall functionality of the system into **a main program and subroutines**.

the following diagram shows how this style work which mean process of calls **functions**.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/procedural-programming-1.png" width="600" hight="600"/>
</p>

The main consideration of this style is the behavior of functions and how data moves through them, so procedural programming supports abstract data types. so this paradigm stored data as variables like object-oriented programming, However, **inheritance** is not supported. But this style is suitable for computation-focused systems.

The principle of this paradigm is "One entry, one exit per subroutine" so each subroutine have its own local variables and has access to all data within its scope, to get access to variable out of scope, you should pass the data as a parameters by value or by reference.

This architectural style focuses on modularity and function reuse. So you can think of them as black boxes meaning gives it a particular input, you always expect the same output. Further, library functions are easily integrated into programs

The issue of this approach is that subroutines may change data in unexpected ways, meaning a subroutine may be affected by data changes made by another subroutine at execution, throwing Runtime errors.  

**Example of spending report.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/procedural-programming-2.png" width="600" hight="600"/>
</p>
