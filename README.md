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

### History of Web Systems

In order to understand the web standards and technologies of web services, and the rise of web applications, we must first study the origin and evolution of web-based systems.

Let us begin with the terms “**Internet**” and “**World Wide Web**”, which are used interchangeable. However, these terms actually refer to two different, but interrelated things. The Internet was actually invented almost 20 years before the World Wide Web!

In 1969, a small computer network called **ARPANET** was used by researchers in the United States to send a small amount of data between computers. This was the first time data was sent across a computer network. In the following years, small networks were developed at research institutions across the United States. Further, these networks began to connect with each other. Once this network of networks reached a global scale, the Internet was born.

The Internet offered potential to communication information across the global. Tim Berners Lee was inspired by the way the brain links information together through association, and began to investigate how documents could be linked together over networks. This led Lee to propose a web management system which was inspired by hypertext and built on top of the Internet, known as the World Wide Web, in 1990.

The World Wide Web, otherwise known as “**the web**” led to standards and technologies for computer-based communication over the Internet. Web standards include **Hypertext Markup Language (HTML)** which standard used to expressing web content, and **Hypertext Transport Protocol (HTTP)** which is standard used for making requests, receiving message, and communicating content**.**

In 1990s, the introduction of HTML and web browsers greatly increased the popularity of the web which allow users to view websites.

Websites are made up of web pages. To view a web page, the web browser makes a request to the web server that hosts the web page, then the web server handles the request by returning the HTML document that corresponds to the requested web page, and then the browser renders this HTML document to the user. The relationship between web browser and web service is a client-server relationship. Both the request and the response are messages conveyed in **HTTP**, a communication protocol that both the web browser and web server understand.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/history-of-web-1.png" width="200" hight="400"/>
</p>

**Static Web Pages**

Originally, the web consisted of **only static web pages**. Each static web page was stored on the server as a separate HTML file.

When a static web page is viewed on a web browser, the HTML rendered on the screen is the same HTML document stored on the web server. The document on the web server has not changed or been customized before being served to the client. In order to change the web page, the corresponding HTML document must be changed. Under this model, even small changes to a web page may require the **update of many HTML documents** to maintain consistency across the whole website. Since changes require manual developer intervention, static websites are best used for **presenting information** that does not change very often, like personal websites or publications.

**Dynamic Web Pages**

In 1993, dynamic web pages are generated by an application at the time of access to solve lack of customizability and scalability by static Web pages. This means that the web page does not exist on a server before it is generated.

The main difference between static and dynamic web pages, is static pages stored on the web server, while dynamic pages are built by web server when they are requested.

For dynamic web page, the web server passes on the request to an application to be handled. The application can perform a computation, look up some information in a database or request information from a web service, which produces a dynamic content as output. The application can generate an HTML document for the server, and then the server sends that back to the web browser, which can then display it for a user.

As a developer, it is easier to make changes to dynamic websites compared to static websites, because you only need to change on database element or variable in your application to make change anywhere on the dynamic website.

Dynamic web pages provide many advantages. 

- They can be customized for the view,
- they can respond to external events,
- they generally provide increased functionality compared to their static counterparts, and
- they are easier for a developer to modify.

Currently, dynamic web pages dominate the web, including many types of webpages such as **personal blogs and news feeds**.

Also may static or dynamic web pages suitable, there are a lot of complexity like, Do the contents of the web page change depending on when you visit the site? Do other people visiting the same web page see different content than you? Do you need to provide extra information, such as a login, before you access the web page? so it time to use **Web Applications.**

**Web Applications**

As growing in web-based systems, web applications like desktop applications, provides graphical user interfaces (GUI) that **allow users to interact with them**. The big difference is desktop application runs and are stored locally on your computer, whereas web applications runs in your web browsers and are store on a **remote web server**.

**Web applications are platform independent**. This means that they can run on any operating system, provided that a compatible web browser is installed. Web applications eliminate the need for users to download and maintain application software on a computer. However, web applications also require users to have **Internet access**, because web applications communicate information through **HTTP** with a **web server and application server on the backend**.

You need to be always online, web applications provide users with a richer, more interactive web experience than simpler dynamic or static web pages. Web applications enable everything from online banking, online learning, online games, calculators, calendars, and more. For example Google Docs is a web application which is browser-based word processor, enable multiple users to collaborate on a textual document in real time.

Modern website or web application will integrate with other **web services** to provide certain content.

**Web Services**

Web services can be used to satisfy specific needs, like stock market data, weather reports, and currency conversion and use of real time information to create more complex applications. Information produced by these web services can be used by many different web applications at the same time. Web applications and web services communicate over the web using open standards like HTTP, XML, and JSON, which are easy for machines to manipulate.

Services provide a user **interface** that can be embedded in a web page or application. By using web services, request and response of different services is **asynchronous**. This means that the logic is designed to continue running instead of waiting for a response. A page composed of many services can be generated while the individual services are processing requests and sending responses.

For example, you were developing a personal landing page, it may have its own content like blog or a writing portfolio, it also uses external services, like showing your latest post from Microblog service provider, or an external Photo-storage service provider. you may get information from your calendar and your travel itinerary, integrated into applet to tell people when you have free time to meet and where you will be. Each of these services produces content for the landing page. So the request is **asynchronous.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/history-of-web-2.png" width="400" hight="400"/>
</p>
