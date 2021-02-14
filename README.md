## Importatnt Note
> Before starting reading this, you can see [Software Architecture](https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/tree/main/Software%20Architecture) article, which we will introduce the most common architectures, their qualities, and tradeoffs. We talked about how architectures are evaluated, what makes a good architecture, and an architecture can be improved. We'll also talk about how the architecture touches on the process of software development.

## Introduction to Service-Oriented Architecture and Web Services

In real world, human use services to make his life easy instead of doing everything by self, like a laundromat, a restaurant, and ride services like Uber. **The same in software industry**, deploying a service means providing a tool that other software can use.

A service, as opposed to a component, **is external to the software requesting it and often remote**, either in another server in the company or somewhere out there on the internet.

Services are often associated with two roles like Client/Server roles:

- **Service Requester** which is the software requesting the service.
- **Service Provider** which fulfills/receive the request.

**Service-oriented Architecture is all about how to build, use, and combine services**. Instead of building large software suites that do everything, service-oriented architecture is all about achieving your software goals by building and using services, and designing an architecture that supports their use.

Software-Oriented Architecture has two contexts:

- **on the Internet** (also known as “**external**” to an organization)
- **in large organizations** (also known as “**internal**” to the organization)

**Web Services**

Web services refers to services that offered on the Internet. It is possible to **build feature-full apps on the Internet** by using existing web services on the web, external to your application to fulfill some of the tasks. For example, a web application for travelling may take advantage of services that obtain flight prices on the internet, services that obtain hotel prices, or car rental services. Essentially, **a number of services had to be combined to create an application**.

The ease of using existing services must be balanced against **qualities of the services**, which is not under the control of developers. In these cases, **non-functional** requirements become very important. These might include:

- **Response time**: if you are rely on a service, you may want to know how quickly it can be provided.
- **Supportability**: do you trust the service provider and the service? will it always be available in the future?
- **Availability**: is the service always running and available for use?

**Services in Large organizations.**

In large enterprises or organizations, in-house code can be turned into services that can be used by different parts of the businesses or combining two more services, these services can be built by adding interfaces to used. For example IT department in organization tracks "**support cost"** in their software, if any other department like management or accountment need this information, instead of sending over email, it offered as service and provide interface to let other departments to query this service as needed. So **internal** service-oriented architecture encourages organizations to build general, reusable software services that can be used and combined as needed. 

One of the disadvantages of full switching to service-oriented architecture (SOA) is **costly**, and it can be **difficult to support** despite its benefits, services are often introduced bit by bit, separating out the most useful, cross-departmental functions first.

The SOA is not easy, the idea sounds simple, but in fact, the modularity and platform independence need to make services effective, don't come by accident. Also SOAs are powerful, as they provide modularity, extensibility, and code reuse. Applications can be built through combining services. New services can be created by combining existing services, either from the ground up, or through the addition of interfaces to existing code.

### Service Principles

In order to provide services that are useful and reusable, there are best practices for services and SOA. These best practices, guidelines, and principles that have been developed that outline the desired properties that services should have. The principles like following:

- **Modular**: services should be modular and loosely coupled, which services are meant to be mixed and matched. Loose coupling in SOA mean that requests are made by passing communication to the service is a way that aligns with its interface. The service performs the necessary operations then passes back a communication containing the results of the service (response).
- **Composable**: services should be used in combination to create usable applications or other services. In order to be composable, the services must be modular, services should able to provide a desired end-goal.
- **Platform and Language Independent**: a good service is platform and language independent, for example, a service which is coded in `Java` can be used by a requester coded in `Ruby`. This achieved by following communication standards and protocols. For example on the internet, services are often requested with an `XML` file or an `HTTP` request.
- **Self-Describing**: a service should describe how to interact with it (describes its own interfaces). This includes what input it takes and what output it gives. There are formal standards for describing services using `WSDL` which stands for **web services description language**.
- **Self-Advertising**: services must make known to potential clients that it is available. Distributed applications using web services have standers like `UDDI` which stands for **Universal Description, Discovery, and Integration** to connect service providers with potential requesters.
