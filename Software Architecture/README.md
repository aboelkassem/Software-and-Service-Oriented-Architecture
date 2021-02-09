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

## Repository-based Systems

As a software developer, any software architecture you create needs to be capable of sharing information between separate components and stored them in organized database.

### Data Centric Software Architecture

This architecture allow you to store and share data between multiple components, also helps to increase the maintainability, reusability and scalability of the system by integrating a shared data storage like databases.

**Two components of this architecture**

- **Central Data**: used to store and serve the information across all the components connected to it.
- **Data Accessors**: is any component that connects to the database, they make queries and transactions in the information stored in the database. Query the database to obtain shared system information. Save the new state of the system back into the database using transactions.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/data-centric-architecture.png" width="600" hight="600"/>
</p>

**Database**: is used to store data, it make sure the data is accurate and consistent over its lifespan (data integrity), also make sure the data will live on after a process has been terminated (data persistence). **Relational Database** are a type of database that uses **tables**.

Relational Database uses **Structured Query Language (SQL)** to query or ask the database for information and perform transactions or tell a database to do something. Management and optimization of queries and transactions can be automated by **Database Management System (DBMS)**.

**Data accessor** contains all the the business rules required to perform its functions.

**Advantages of Data Centric architecture over a basic object-oriented system.**

- This architecture supports data integrity, data backup and data restoration through a database which can help if there are massive data loss, data corruption or data migrations.
- It reduces the overhead for data transfer between your data accessors, meaning the data accessor doesn't to be concerned with talking to another.
- A system that can be easily scaled up, as data accessors are functionally independent, so additional features can be added with having to worry about affecting others.
- Central data components “live” on a separate server machine with sufficient disk storage dedicated to the database (centralized data repository), which allow for easier management of information

**Disadvantages of Data Centric architecture**

- Using centralized database, the system becomes heavily reliant on the central data component. If the data server goes offline, becomes unusable or contains corrupted data your entire system will be affected, for solving this issue there are data redundancies to replicate your data onto separate hard disks but the physical infrastructure can be expensive and costly to get your system back up and running again.
- Also your data accessors are dependent on what gets stored in the database. New data accessors need to build around the existing data schema. if there is no matching column or table for a specific data need, then the database cannot be used to save this data.
- It is difficult to change the existing data schema, which will affect your data accessors.

**For Summary, The data centric software architecture allows you to:**

- **Store and manage large amount of data into a central data component**. This increases your system's stability, performance, reusability and maintainability.
- **Separate the functionality of your data accessors**, which makes it easier for you to maintain and scale your entire system.
- **Facilitate data sharing between data accessors through database queries and transactions.**

## Layered Systems

In software applications the inner layer (bottom layer) providing services to the one outside it and vice versa. Each layer can communicate with its adjacent layers, For example the following diagram of school system. Principal layer interact with Student layer through Teachers layer, Teach Layer interact with both layers Student and Principal, Also Student can interact with other students. 

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/layered-system-example.png" width="500" hight="500"/>
</p>

A layer is collection of components that work together toward a common purpose. The components in a layer only interact with components in their own layer or adjacent layers.

Layering allows for separation of concerns into each layers, So many layered system are split into **Presentation, Logic and Data layers**.

The Operating System (OS) for a computer is an example of layered system:

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/layered-system-example-1.png" width="200" hight="200"/>
</p>

- **Kernal**: is the core of an OS, it main responsibilities it interfacing with the hardware and allocating resources like schedules operations for the processor or reads the input from your mouse/keyboard.
- **System and Application Libraries**: is used to providing high-level functions (API) that the programs need to interface the kernel like functions for saving file or drawing graphics.
- **Utilities and Applications**: Utilities are tools included with the OS like command line program or file browser, Applications are programs that installed by the user, this layer rely on the layer below to use system resources.

**The most benefits and advantages of this layered structure.**

- Is that users can **perform complex tasks without understanding the layers below**. Like programmers can create applications that rely on the libraries layer without needing direct knowledge of the kernal.
- Is that the different layers can be run at different **levels of authorization**, For example the Top layer is run in **User Space** which doesn't have the authority to allocate system resources or communicate with hardware directly. this done by **Sandboxing** which improves the security and reliability of the kernal.
- Your design will be more **loosely coupled and modular code**. which Layered architecture follows **the principle of Least Knowledge**.

If you do replace a layer, you only have to ensure that its interface with the layer above is consistent with the previous implementation. So why use Layered Systems? because its powerful architecture and many organizations and solutions have a layered structure. And easily mapped to organize a solution of many problems and design complexity.

### N-Tier Architecture

Tiers is similar to layers but often refer to components that are on physical machines. **3-Tier and 4-tier** architectures are common used but any number is possible.

**2-Tier Architecture**

The relationship between **2-Tier** is a **Client/Server** relationship. Which the **Server** side provides services like storing information in database or performing computation tasks. **The Client** side requests these services through messages so the communication between the two sides called **Request-Response**. Which the client request information or actions and the server responds.

**Example of 2-Tier Client/Server architecture that shows media server**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/n-tier-1.png" width="500" hight="500"/>
</p>

One computer hosts the media server process, where movies and TV shows are stored and can be streamed on demand. When a client requests a movie or TV show, the media server streams it to the client. Also you can make media server machine in one machine Desktop to play as media player or media server.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/n-tier-2.png" width="300" hight="300"/>
</p>

The above Sequence Diagram illustrates the **Request-Response** Messaging relationship. This relationship between client and server can be **Synchronous** or **Asynchronous**.

- In **synchronous**, the client send a request then awaits the server's response before continuing execution.
- In **asynchronous**, the client sends a request, but control returns right away so it can continue its processing on another need, so the processing not depend on server's response. Once the server has completed the request, a message is sent to the client, which will have a handler to process the response. So its a better option.

**Client-Host** and **Server-Host** refer to machines that host the client and client software. There are many types of servers like Web Servers, Media Servers, Application Servers, File Servers, Data Servers and Print servers.

Limiting **client/server** relationships to **request/response** messaging patterns allows for systems that can be **scaled** more easily by adding clients. Clients and servers are extensible, because as long as a server receives a message it knows, it will respond. The source of the message is not important to the server, so many clients can be added as needed.

**Another example of 2-Tier Architecture**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/n-tier-3.png" width="500" hight="500"/>
</p>

Problem: if the database changes, you are going to have to change the software on each and very computer. To make an improvement by inserting a tier in between data and end user to become **3-Tier Architecture**. 

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/n-tier-4.png" width="500" hight="500"/>
</p>

**This layer** has many names like **Middle** layer, **Business** layer or **Application** layer. It's a client of the database and a server for the client application on the end users' devices. It's used to determined how and when data can be changed. So now  the client software makes request to the application tier, which makes data calls, so its easy to maintain.

N-tier architecture follows on separation of concerns, for above example the application logic could be split into **security** concerns and **database operation** concerns.

**Drawbacks of the N-tier architecture.**

- It **demands extra resources** to manage the client/server relationships, meaning adding more tiers means adding more machines to manage with different communication protocols between machines which make the system more complex.
- A **server acts a central point of failure**, Systems may have backups or mirrors, but it can take time to switch to these backups and recover the server. Redundant servers are possible but add complexity.

**Advantages of the N-tier architecture.**

- Very **scalable**. Clients can continue to be added as long as a server can handle all the requests it receives in a reasonable time.
- **Centralization** of functionality allow for data to reside on one machine but to be accessible by any machine on the same network.
- **Centralization of computing power** allows client machines to require less processing power. Companies can thus offer processing power as a service, which is more practical and cost effective.
- Supports **separation of concerns**. Middle layers can take the role of managing application logic and accessing the database directly. Adding tiers can further allow for more separation of concerns, loose coupling and levels of abstraction, making a system that is easier to change and extend.

## Interpreter-Based Systems

Systems based on interpreters (Interpreter-Based Architecture) can allow end user to write **scripts** or **rules** that access or run the **basic features** of those systems in new ways like formulas in Microsoft Excel. Which interpreters can run **scripts, macros** and drive programmable actions specified by user.

**Scripts** can write to automate tasks like Schedule tasks, performing repetitive actions or complex tasks. **Macros** are an evolution of scripts and popular with GUI which records keyboard and mouse inputs so that they can be executed later, which allow users to record interactions with user interface like collecting coins in games.

**Interpreter** allows you to add functionality to a system or Extend existing functionality of a system, by composing **pre-existing functions** together to create something new. For example, **web browser extension** is a component that adds new functionality to the browser and can customize the pages that the browser renders which this component written and implemented by language like **Javascript** to run by an interpreter in the browser.

Having a system with built-in interpreter is not only beneficial to **developers**, it encourages end users to implement their **own customizations**. Which the system can offer an easier language suited to the needs and thinking of the end users.

Interpreters make systems more **portable**,  so they can work on platforms that the interpreter supports (languages). This is an important feature with the growth of virtual machines and virtual environments, more and more services are being hosted in the cloud, so you develop and deploy software system onto hardware that you have no control over.

Interpreters can be **slow**, spending little time to analyze the source code and use line by line translate and execute.

**Example of where interpreters are used for java programming languages.**

In Java, programs are first translated into an intermediate language that is loaded into a Java Virtual Machine (JVM), then executes the intermediate language, JVM used to optimize the intermediate instructions monitoring the frequency of the instructions. Which later translated into machine code to execute. On the next execution of the same intermediate instructions, the JVM uses **Lazy Linking** to point the program to the previous machine code translation. Instructions that are not used frequently are left for the **interpreter** of the JVM to execute.

This decrease execution time since frequency used instructions don't need to be constantly translated and the entire program doesn't need to be translated all at once. Also the JVM also provides portability to Java programs, allowing them to run on many operating environments.

## Pipe and Filter Architecture

Pipe and Filter architecture is a type of Data Flow Architecture, **Data Flow Architecture** consider a system is series of transformation on data using different type of operations.

A pipe and filter architecture has entities called **Filters**, which perform transformations on data input they receive. **Pipes** which server as connectors for the stream of data being transformed.

**The following diagram show the data flows in one direction**. The changes of the data are done sequentially from filter to filter.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/pipe-filter-arch-1.png" width="500" hight="200"/>
</p>

The order in which filters transform data may **change the end result**, the input of one filter is the output of another, so order is very important. Also it used as the text based utilities in the Unix operating system.

**UML Component Diagram of Pipe and Filter Architecture.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/pipe-filter-arch-2.png" width="500" hight="200"/>
</p>

**Advantages of Pipe and Filter Architecture.**

- **Ensures loose and flexible coupling of components**, because each filter runs independently, so it's only focuses in its input and its output, also easy to move filter around in a system to achieve different results. Also made easily changes on individual filters without affecting other filters in the system.
- **Filters can be treated as black boxes**, users don't need to know the inner workings of each filter.
- **Reusability**, is the main advantage of this architecture, each filter can be called over and over again with different inputs.

**Disadvantages of Pipe and Filter Architecture.**

- **May reduce performance due to excessive overheads in filters**. because each filter parse the input into a data structure, do transformations and send data to another, if every filter has to do this process will cause overheads, so the performance of the system will reduce.
- **May cause filters to get overloaded with massive amount of data to process.**
- **Cannot be used for interactive applications** because it will take time to process data depend in filters.

## Event-Based Architecture

This architectural style derives from the **Event Driven Programming paradigm**. in this style, the main elements in the system are **events**. Which can be signals, user inputs, messages or data from other functions. Events act as **indicators of change** and **triggers**. In This paradigm **functions** can be **event generators or event consumers**. Which event generators send events, event consumers receive and process these events.

In the event-based architectural style, functions are not explicitly called. Instead, **event consumers are called based on events sent from event generators**. Event-based functions communication between functions by **an event bus** not with each other. Think of event bus as the connector between of all event generators and consumers in the system.

To achieve this structure, bind an event and an event consumer via an event bus. This means that each event consumer registers with the event bus to be notified of certain events, when event bus detects an event it distributes the event to all appropriate event consumers. Like **observer design pattern** which based on this architectural style.

To implement the event bus there are one way, having a **main loop** in the system that continually listens for events, when an event is detected, the loop calls all the functions bound to that event. An event consumer will have to notify other functions when it has completed its task or to send a state change. This function will invoke other functions to run after it has completed. It does this by sending out an event to the event bus. When an event reaches the event bus, corresponding event consumers will be triggered and the next computation can take place.

**Example of Code Editor to understand this process in UML Component Diagram.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/event-based-arch-1.png" width="500" hight="500"/>
</p>

Notice in this example the Build Tool, Test Tool and Editor are all event generators and consumers. The best thing in this architecture is the event consumers don't necessarily know who is generating the events they handled, This loose coupling of functions makes system easier to scale and evolve, adding new functionality for an existing event is as simple as registering a new event function to event bus and add new event consumer.

In this architectural style, events and function don't occur in a predictable way, there are no guarantees of exactly when an event will be handled, how long it will take to be handled or when an event generator will emit an event. Control flow is based on which events occur during its execution and in what order.

This style will be suitable to interactive applications, applications that rely on user input and distributed systems that interact with other programs.

**Cookie Clicker Example to apply event-based architecture.**

 “Cookie Clicker.” The goal of this game is to collect as many points as possible by clicking on an image of a cookie with your cursor. This can be done manually or by clicking on a cursor icon.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/event-based-arch-2.png" width="400" hight="400"/>
</p>

When Click in the cookie manually, the total points will increase by one point, The Buy Clicker icon has a functionality, it will purchase a special automatic clicker that automatically clicks the cookie at regular time intervals with 5 cookie points, thus reducing work on the user’s part to collect points.

The following Component Diagram shows the system using event-based architecture.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/event-based-arch-3.png" width="500" hight="500"/>
</p>

The "timer" function is an event generator, added to system by first "buy clicker" event, registered to the event bus, that sends a timer event every five seconds, When "timer" function emits a timer event, the event bus detects this and trigger every "Automatic clicker" function to consume this event.

## Software Architecture in Practice.

Software architecture aims to combine **software design patterns and principles** in order to define the software's **elements**, properties and interaction with each other. If the architecture of the system is just a set of design patterns and principles, then you can determine the capabilities and the quality of the architecture based on the elements. However, this is not the case, because design patterns are good at addressing one specific technical problem but poor at addressing the wide range of business needs and concerns. So modern systems need to be able to focus on a **wide range of problems, not just technical issues.**

System architecture are more concerned with addressing the bigger picture including **functional** and **non-functional** aspects of the system. It will set guidelines for design patterns and principles in order to make the system has conceptual integrity and consistency. In addition to design patterns and principle to define **functional issues** which improve system's maintainability, reusability and performance, but software architecture must consider **non-functional requirements** like testability, usability and availability. So software architecture addresses these qualities in addition to design patterns in order to **construct a unified system** to be qualified by how well the design addresses user experience and ease of development.

**So, How architecture be Good or Bad?** Software architecture is not good or bad. That is to say that an architectural design doesn't have qualities or it's correct that make it a "good architecture" or "bad architecture". Software architecture is designed to address a set of requirements that are used to address a problem or need. **For example** an online web-based game will use event-based architecture over repository-based architecture in order to facilitate communications between players. Also your system will most likely use a combination of architectural designs because the modern requirements are complex and there are no architecture that is capable with all the requirements. So it's important to consider the **context** of the problem and requirements.

There are functional and non-functional requirements when designing the architecture of your system, software must address all the functional requirements but you also need to design to meet non-functional requirements as well. Non-functional requirements are not always clear or presented by your clients or stakeholders. These requirements can differ between each group, for example development team will care about maintainability, reusability, testability and supportability. End users doesn't care about that but care about ease of use, error handling and system stability.

### Quality attributes.

**How measure an architectural design to determine if it is capable of meeting the system requirements?** It is determined by **quality attributes**. Which they are measurable properties of a system used to measure of a system's design, runtime performance and usability. For an attribute to be measurable, there needs to be an objective means of quantifying it. For example, system availability can be measured by the system’s **uptime** in some unit of time.

The following table shows attributes that covered when design a system using design patterns and principles (from developer's perspective).

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/quality-attributes-1.png" width="400" hight="400"/>
</p>

- **Maintainability** determine how easy systems can undergo changes like fix errors, change software elements, add new features or retire old services.
- **Reusability** allows you to take functionality or parts of a system and use it in another one. which help to reduce of reimplementing something that has already been done.
- **Flexibility** is the ability to adapt future requirements changes in a timely and cost efficient manner.
- **Modifiability** like maintainability, determines the ease at which your system is able to handle changes to functions, adding new functionality or remove existing ones. Also adopting new technologies and industry standards.
- **Testability** define testing your program from errors and bugs to be fixed before release your system.
- **Conceptual Integrity** determine which there is consistency throughout the system.

In addition to qualities to account for from a **developer’s perspective**, it is also necessary to take into consideration qualities from a **user’s perspective** in the following table.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/quality-attributes-2.png" width="400" hight="400"/>
</p>

- **Availability** is measured by its **uptime** because you want to know how well it is capable from issues like system errors, high loads or updates, and try to prevent them.
- **Interoperability** is the ability to understand interfaces and use them to exchange information under specific conditions with external systems, meaning how your system response to other systems as outlined in the documentation. Modern system has a define context which it exchanges information including communication protocols, data formats and with whom allowed to exchange information.
- **Security** should be considered to prevent sensitive information to be accessible to users that are not authorized to see it. System should only provide data integrity, meaning controls who can see the data versus who can also change the data.
- **Performance** is measured by the amount of output over a period of time to produce this output after receiving an input.
- **Usability** achieved by your system needs to be easy and intuitive to learn, minimize user errors, provide feedback to the user to indicate that the system has registered their actions, and make it easy to complete tasks.

**How do we go about design a high quality system?** the important matters is being **create, or choose an appropriate architectural design for your system** because architecture is determine how functionality is implemented, how subsystems communicate with each other and how end users interact with your system. If the qualities achieved by the architecture are good, it makes maintaining, supporting, and updating the system throughout its life cycle much easier.

A high-quality system does not need to be “**complex**.” An overly complex system makes it difficult and time consuming to produce. It is good practice to try to minimize complexity in the design. If a **simpler** architecture can satisfy all the system requirements and achieve a high-quality design while needing less time and less money, it makes sense to go with that.

Having detailed and **up-to-date documentation** making it high-quality system, Which helps record and share an architectural vision to coworkers to know how functionality of the system are designed.  The documentation keeps a design cohesive, if the architect or any of the developers leave the team.

You should use a set of **rules or guidelines** for the design process and how your system will be structured. It vary from company to company but there are general guidelines like:

- Recognizing the importance of quality attributes and prioritizing them for each system being design.
- Involving a technical lead in the design process. Although architectural design can be applied to many different technologies, involving a technical lead will help identify any implementations that may pose a challenge, which may need to be re-considered in the design.
- Taking a design approach from the perspective of the different groups of stakeholders.

You can write your own guidelines to ensure there is conceptual integrity when implementing the system like:

- Having well defined subsystems that are assigned responsibilities based on design principles.
- Having consistent implementations of functions across the entire system.
- Having a set of rules on how resources are used like memory, bandwidth or threads.

In summary, remember that architecture is not good or bad, it is a matter of selecting the appropriate architectural solution for your problem, it is important to involve all groups of stakeholders in the design of the system, to adopt good documentation practices, and to set rules for design and implementation

A well-designed system considers quality attributes from a developer’s perspective, which includes maintainability, reusability, flexibility, modifiability, testability, and conceptual integrity; the system should also consider attributes from a user’s perspective, which includes availability, interoperability, security, performance, and usability.

### Analyzing and Evaluating an Architecture

Software systems are designed to address the specific business needs to various stakeholders, So we need to use a methodical way of analyzing and evaluating a system's behaviors, quality attributes , and various characteristics to meet a specific set of standards.

In order to measure quality attributes, they use **quality attribute scenarios** to determine if a system is able to meet the requirements. There are two types of scenarios:

- **General scenario** is used to characterize any system
- **Concrete scenario** is used to characterize a specific system.

In the context of analyzing and evaluating architecture, you should focus on situations that are **outside of the normal execution path**. This means that scenarios involving incorrect input, heavy system loads, or potential security breaches should be prioritized highly.

**Scenario** is a system's ability to handle unexpected failures that stops from achieving a specific quality attributes.

Each scenario consists of:

- **Stimulus source**: is anything that creates a stimulus, a source can be internal or external to the system like internal timer for internal system, or end user for external system.
- **Stimulus**: is a condition that will cause the system to respond, conditions like internal specific error could be a buffer overflow, or external specific error could be incorrect user input.
- **Artifact**: is the part of the system that is affected by the stimulus. In large-scale systems, a stimulus should not directly affect the entire system.
- **Environment**: is the mode of the system when it is receiving a stimulus.
- **Response**: is how the artifact will behave as result of receiving a stimulus like handling an error, recovering from a failure, updating system logs, dispatching security alerts, or changing the current environment.
- **Response Measure:** a metric used to quantify the response so that the quality attribute can be measured, like probability of failure, response time, repair time, and average system load.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/evaluate-and-analysis-arch-1.png" width="400" hight="400"/>
</p>

**Availability Quality Attribute Scenario Example**

Imagine you are addressing the availability of a system. In addition to focusing on when a system is online and behaving normally, you have to consider situations where the system becomes unavailable, and measure how long it takes to recover.

**In a general scenario**, high-level events are summarized:


<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/evaluate-and-analysis-arch-2.png" width="400" hight="400"/>
</p>

**In a concrete scenario** which allows you to test an architecture with a specific stimulus, under specific system environments, and measure how well the system can respond. For exmple

- Availability for a web server can measured in a its ability to process requests when at resource limits or under heavy load, so you can measure a server's availability under different conditions.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/evaluate-and-analysis-arch-3.png" width="400" hight="400"/>
</p>

**Architecture Trade-off Analysis Method (ATAM)**

This technique developed by Software Engineering Institute at Carnegie Mellon University, used to analysis and evaluation of the entire architecture. Which its main advantages that evaluators/architects don't need to be familiar with the architecture or the problem space.

ATAM involves three different groups of participants:

- **Evaluation Team** which has:
    - **Designers** which are the ones involved with the architectural design. these follows an iterative, Hypothesis-Driven method when designing which involves analyzing requirements, creating a design, reviewing the design to see if it works.
    - **Peers** which are not involved in the design decision, but Their point-of-views helps round out design decision.
    - **Outsiders** who external to the project or organization, helps to eliminate bias towards the project and have experience in analyzing architecture.
- **Project Decision Makers** these have the authority to make project decisions, including project managers, clients, product owners, software architects, and technical leads.
- **Architecture Stakeholders** which includes anyone who want the architecture to successfully address business needs but who are not actively involved in the evaluation process, like end users, developers, and support staff.

The following diagram shows high level flow of ATAM:


<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/ATAM-1.png" width="600" hight="600"/>
</p>

In an ATAM, a software project is initiated when business drivers identify a need for a system to address some problem. Business drivers go hand in hand with the system architecture, which is created as the solution to the business issues. Together, business drivers and system architecture determine the quality attributes of the system, the architectural approach taken, and the design decisions that are made. These combine together to create quality attribute scenarios. Scenarios can then be analyzed, resulting in an evaluation of the system, which includes trade-offs, sensitivity points, non-risk scenarios, and risk scenarios. Since the risk scenarios have a negative impact on the quality of the system, each of them are analyzed and categorized into “risk themes".

**The ATAM process and its nine steps**

- **Present the ATAM**. The evaluation team presents the ATAM process, which includes the context for the evaluation, expectations, procedures, outputs, and address any other concerns.
- **Present the business drivers**. This project decision makers present the business problem, and the goals of the system, system's features and requirements, project constrains, and scope.
- **Present the architecture**. The current and expected state of architecture is presented, constraints of the project that can affect the architecture such as time, cost, difficulty of the problem, and quality expectations.
- **Identify the architectural approaches**. This is the first analysis activity which involves examining the architectural patterns that have been used in the system so far. In this step you analyze the documentation, the notes from presentations, and ask questions to get more clarity about the system.
- **Create a quality attribute tree**. The requirements for each quality attribute is details in a utility tree. which captures all the quality related architecturally significant requirements (**ASRs**). Which get from business drivers to utility system's quality attributes. You can insight about the system and identify the quality priorities by working with the project decision makers to refine your tree.

    
  <p align="center" width="100%">
    <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/ATAM-2.png" width="600" hight="600"/>
  </p>

    To build such a tree, the overall “utility” of a system is broken down into quality attributes, which are refined into attribute refinements. **Attribute refinements** are more specific qualities of a system. Once the quality attributes have been refined, ASRs can be associated with the appropriate attribute.

    In quality attribute trees, ASRs are given priority values to denote if they are “must-haves” or not. The example above uses high (H), medium (M), and low (L) designations, but these values could differ from system to system.

- **Analyze the architectural approaches**. Using the prioritized ASRs from utility tree, examine the architecture and determine how it addresses each ASR. this allows you to identify and document the risk and non-risk scenarios, sensitivity points, and trade-offs. Sensitivity Point can affect the quality attributes, For example high traffic may cause an increase in the system's latency. Trade-offs occur when sacrifice one quality for improvements in another, For example you could limit the number of concurrent users allowed on your system, this limit the system's availability but don't worry about increasing latency while system grows up.
- **Brainstorm and prioritize scenarios**. Each group of participants creates quality attribute scenarios that are important to them, and that they would expect when using the system. Scenarios that have similar quality concerns or behaviors can be merged together. Scenarios are prioritized based on importance to each stakeholder, and the evaluation team compares the list with the prioritized ASRs in the utility tree. If the priorities of the stakeholders match closely with the priorities in the utility tree, then there is **good alignment.**
- **Re-analyze the architectural approaches**. Similar the earlier analysis, you create a utility tree, but you will use the top five or ten scenarios prioritized in the previous step.


  <p align="center" width="100%">
    <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/ATAM-3.png" width="600" hight="600"/>
  </p>

- **Present the result**. Finally the results of the evaluation are compiled and presented. This risk scenarios are grouped together, and categorized into "risk themes". Risk themes help to identify which business drivers are affected. The information presented includes all architecture documents, utility trees, risk and non-risk scenarios, sensitivity points, tradeoffs, and risk themes.

Modern systems are becoming more and more complex as technology grows, and creating an architecture that can achieve all the requirements for quality attributes is becoming increasingly important. Being able to evaluate and analyze architectures helps successfully create high-quality systems.

ATAM is a common method for analyzing and evaluating architectures, especially as it does not require evaluators to have intimate knowledge of the system, and covers the viewpoints of all important stakeholders. ATAM helps minimize risks in a system by identifying them and helps architects minimize the effects of sensitivity points and be sensible about trade-offs. Also helps facilitate communication between stakeholders, Found issues with the newly discovered functionalities, elevated the role of software architecture.

## Product Lines (Product Families)

As developers work, they should always be looking for opportunities for **code re-use**. The software world is full of code re-use implemented in different ways. Such as libraries, toolkits, and engines. Which save time for developers and get robust solutions by reusing code. Reusing code is much faster than developing new code. Even if code has to be modified or adapted to the application, its still faster that writing from scratch. So well-written and well-documented code is important. 

**Product lines** are groupings of products that typically **share the same operating system**, which allow for a great deal of code re-use. For example IOS which is developed for product line of iPhones, iPads, and iPod touch products.

**Product lines present several advantages:**

- **Cost**. Product lines designed with similar features allow companies to **save money** because it reduces their development costs per product. The time saved on development can be spent testing for quality attributes, such as reliability, user experience, security, and maintainability. However, less testing is needed overall per product, because code that is reused has already been tested.
- **User Experience**. If several products share characteristics, then the learning curve for customers and developers is smaller and fewer surprises. This may also drive sales of other products in the same line. Which is a key strategy of Apple company.
- **Time-to-market**. Since most software components are already made, making a new product in the product line, or refining an existing one, takes less time.

If only one or two products are being produced, it might not be worthwhile to treat them as a product line, unless there is intent to develop more products later on.

**Implementing Product Lines:**

Separate the features that stay the same from the features that are different across products.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/product-lines-1.png" width="500" hight="500"/>
</p>
  
- **Commonalities** like the user experience of the apple products.
- **Variations** like supporting for different cellular network connections in the line of tablets, IPhones.
- **Product-Specifics** like the tablets which developed specialize in reading eBooks. Its product specifics could be additional tools for managing eBooks and support for an e-ink screen

Product line development teams are generally divided into two camps:

- **Domain engineering**: is the development of the commonalities and variations. Essentially this is putting together the building blocks of the products or the infrastructure.
- **Application Engineering**: is the actual development of the product. It includes using the commonalities, deciding which variations are necessary, and integrating them into the product and developing product-specific features. This is sometimes described as “instantiating” a product. There could be several application engineering teams, one for each product.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/product-lines-2.png" width="600" hight="600"/>
</p>

Separating development into domain and application engineering allows for **separate development cycles**. The domain engineering team can determine the long-term needs of the product line, evolve and test components as needed, then **release that infrastructure to the application team**. Then, the application team can develop product specific features using the infrastructure and the requirements of the product. They will develop product-specific features, decide what variations to use, and test the final product. This can be done while the domain engineering team is working on the next update of the infrastructure.

### Reference Architecture

Products in a product line likely have similar architectures, as they serve a similar purpose. Instead of creating a new architecture from scratch for each product, the product line usually has an architecture that products can build on or change. **The domain team** is generally responsible for this **reference architecture**.

**The reference architecture must:**

- be designed with respect to the needs of the software, while taking into account all current products in the product line.
- include the capacity of variation, for differences in products and to allow for future products in mind.

Because there will be differences in the product line, there are **three general techniques** to realize **variations** in a system:

- **Adaptation technique**. In this technique, the component has only one implementation, but it supplies interfaces to change or add on to it. Components can be adapted through **settings in a configuration file**, by adding new methods or by overriding existing methods

  <p align="center" width="100%">
    <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/product-lines-3.png" width="300" hight="300"/>
  </p>

- **Replacement technique**. In this technique, there could be a default component that is replaced with alternatives to realize variation. There may not even be a default; instead there is a gap in the system, and the developers must supply one of the components.

  <p align="center" width="100%">
    <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/product-lines-4.png" width="300" hight="300"/>
  </p>

- **Extension technique.** In this technique, a common interface is provided for all the variations of the system. These variations are often called extensions, add-ons, or plugins.

  <p align="center" width="100%">
    <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Software%20Architecture/Images/product-lines-5.png" width="300" hight="300"/>
  </p>

Variations can be realized at different times. Different variations may even come in at different stages they can be formed early on, during the design or development process of the application engineering team, or they can be formed when the software is compiled and built. Similarly, variations can be realized at different times, like when the software is launched or after the software is launched, whenever they are needed.

Product lines are an efficient way to use the power of code re-use in related products, which save time and cost. Usually this is done by splitting development into domain engineering and Application Engineering. Product lines impose new requirements on the architecture. The reference architecture applies to all products in the product line, and must handle both commonality and changes. The extra resources and the common code in product lines can be used for all kinds of good. Like reliability, user experience, security, time-to-market, and maintainability.
