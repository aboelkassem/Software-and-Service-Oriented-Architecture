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
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/history-of-web-2.png" width="500" hight="500"/>
</p>

### Layers of Web Architecture

Layer is collection of components that work together toward a common purpose. Layers used to **identify hierarchies in the system** and **to restrict how layers interact with each other**. So components in a layer only interact with components in their own layer or adjacent layers through interfaces provided by each component.

Complex systems require more layers to help logically separate the components. However, the disadvantage of adding additional layers is that **performance suffers** due to the increase in communication between the layers.

Layered systems are organized into **Presentation**, **Application**, and **Data tiers**. In web systems, presentation tier is divided into two layers, **web browser** and **web server**.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/layers-web-app-1.png" width="300" hight="500"/>
</p>

- **The Web Browser Layer** is the top layer, it displays the information to the user.
- **The Web Server Layer** is below the web browser layer, it receives a request from the web browser, **obtains the request content** and **returns it to the browser**.
- **The Application Layer** which is responsible for ensuring the function or service provided by the system is performed.
- **The Data Layer** which is responsible for storing, maintaining, and managing data. Access to data read-only or both reading and writing. It can be a file system or database.

Not all systems require this four layers, and not all systems use these layers the same way.

**Layers for Static Web Content**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/layers-web-app-2.png" width="300" hight="500"/>
</p>

The web server layer receives the request from the web browser and grabs the appropriate HTML documents stored in data layer. After it has accessed, it returns the request content to the browser.  There is no application layer in a static web content system, as the HTML documents served by the web server are the exact as stored in the file system. No processing has been applied

**Layers for Dynamic Web Content and Web Applications**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/layers-web-app-1.png" width="300" hight="500"/>
</p>

Web browser and web server perform the same way as above with static content, the web server passes on the request to an application server in the application layer for processing, The application layer may consist of one or more programs that process the request to generate the resulting content. Also The application layer may also call upon other **web services**, and read and write data to a database via the data layer

**UML Component diagram of web systems**

Think of web as a collection of services. For example database provides data services, and the application server is a service requester to the database. The application server runs programs that may access a variety of web services provided outside the system.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/layers-web-app-3.png" width="400" hight="400"/>
</p>

Layered architecture and use of outside web services reinforces the basic design principles of separation of concerns and code reuse. Layers have specific responsibilities, while outside services provide functionality that the system does not have to implement. The scope of using web services is huge, so it raises the challenge of identifying the right ones to use.

### HTML/XML/JSON

Web systems have many different types of formats that can be used to store and express content. Types like HTML,XML,JSON.**HTML** and **XML** are markup languages used to express and structure content. **JSON** is a popular lightweight data interchange format. 

Markup languages are designed to adorn texts in a machine and human readable way, to add meaning or structure. Markup languages rely on **tags** to mark how pieces of text are interpreted. Like:

```html
<adjective>service-oriented</adjective>
<noun>architecture</noun>
```

There is no programming syntax in markup languages. Tags turn a simple text file into something a computer can manipulate or a human can understand.

**HTML (HyperText Markup Language)**

HTML Standard focuses on structuring, not styling the text. It marks what parts of the page text are the title, headings, paragraphs.. etc. Which need to be rendered by a web browser.

HTML has a predefined set of tags that serve different purposes, like the following basic code of HTML document.

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Page Title</title>
	</head>

	<body>
		<h1>This is a Heading</h1>
		<p>This is a paragraph.</p>
	</body>
</html>
```

- **DOCTYPE** is necessary as first line in any HTML file, which tell the browser that the content is HTML.
- **Head tag** contains metadata being used by the page.
- **Body tag** contains the main content and information of your web page. Like the text, links, images, lists, and other data you want to present.

There is no styling in HTML document, but if you want add styling like fonts or colors, you can add CSS (Cascading Style Sheet). This styling can be applied via a separate CSS file, or directly within the HTML document into `<style>` tag in header section. For example color paragraph in blue.

```css
p {
	color:blue;
}
```

**XML (eXtensible Markup Language)**

This markup language meant to store and transport data. XML is used to send structured data within a web systems. You can define an XML schema for the valid tag and their appropriate structure. For example of XML document.

```xml
<?xml version=”1.0” encoding=”UTF-8”?>
<note>
	<to>John</to>
	<from>Jane</from>
	<heading>Reminder</heading>
	<body>Don’t forget the dogs.</body>
</note>
```

**JSON (JavaScript Object Notation)**

Another format that can be used to store and transport data between web browsers and servers. The benefit of using JSON format is the ability to easily convert JSON to **JavaScript** objects, or any languages and vice versa. For example of JSON object 

```json
{
	"firstName":"John",
	"lastName":"Doe",
	"Age":"15",
	"favouriteColour":"Red"
}
```

JSON data is written as **name-value** pairs. JSON data can also have **arrays** of JSON objects which written in square brackets like following,

```json
{
	"Students":[
		{
			"firstName":"John",
			"lastName":"Doe",
			"Age":"15",
			"favouriteColour":"Red"
		},
		{
			"firstName":"Mohamed",
			"lastName":"Abderahman",
			"Age":"21",
			"favouriteColour":"Black"
		},
		{
			"firstName":"Ahmed",
			"lastName":"Mostafa",
			"Age":"19",
			"favouriteColour":"Blue"
		}
	]
}
```
### HTTP

**HyperText Transport Protocol (HTTP)** is a protocol that dictates how information, including hypertexts, is transferred across the Internet.

To understanding HTTP, first begins with Hypertext. **Hypertext** is a document embedded with hyperlinks which used to link HTML documents. HTTP was designed to facilitate the use of hypertext and support the communication of documents and resources expressed in HTML.

Over time, hyperlinks have been used to link together **multimedia** resources, such as images, videos, gifs, text, and audio, or documents containing any combination of these. Resources can be static, such as HTML documents, images, or videos, or dynamic, such as programs that produce some output when they are called.

We will focus on **HTTP 1.1**, although several protocol versions exist.

**URIs and URLs**

**Universal Resource Identifiers (URIs)** are addresses used to **identify resources**, **Universal Resource Locators (URLs)** are a subset of URIs that used to **locate resources**. Both are used to identify the resource, but 

- **URLs** tell the protocol how to locate and access the resource, which provide the protocol, the domain name, or IP address, of the machine that resource stored on and the location of the resource on the machine. So All URLs are URIs, but not all URIs are URLs.

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/uri-url.png" width="300" hight="300"/>
</p>

So as example of URI ⇒ [http://example.com/user/favoriteitems/widebrimsunhat/sunhat.png](http://example.com/user/favoriteitems/widebrimsunhat/sunhat.png)

- **Protocol** ⇒ Http
- **Hostname** ⇒ example.com
- **Location of the resource on the host machine** ⇒ [user/favoriteitems/widebrimsunhat](http://example.com/user/favoriteitems/widebrimsunhat/sunhat.png)
- **Resource** ⇒ sunhat.png

> The URI does not need to explicitly provide the **IP address**. The browser is able to resolve the IP address corresponding to the hostname provided in the URI. or if it doesn’t know, it will query a Domain Name System (DNS) server to find out.

HTTP is built on top of another protocol called **TCP (Transmission Control Protocol)**.

**TCP**

When a client makes a request to a server, this opens a TCP connection between the client and server allowing for communication. Messages are sent and received through **TCP ports.**

**HTTP** relies on TCP connections as they allow for reliable, ordered, connection oriented communication. This mean when a browser accesses a URI that starts with “http”, a connection between the web browser and a web server is opened on **TCP port 80**. This port is the **default** for HTTP messages. For example ⇒ [http://example.com:80/user/favoriteitems/widebrimsunhat/sunhat.png](http://example.com/user/favoriteitems/widebrimsunhat/sunhat.png), and occasionally you cannot see port numbers, as production systems typically use the default TCP ports.

**HTTP Requests and HTTP Responses**

HTTP is build upon a client/server design. The relationship exists between a web browser and web server. So the general format of HTTP request and responses are the following:

- **Request** Consists of :
    - **Request-Line:** This includes the request method (GET, POST, PUT), request URI, and protocol. This URI may end in a query string to specify parameter data for the request. This string is separated from the path by a question mark (?).
    - **Headers**: Client requests may have a various number of headers, of different kinds. It can be used to provide more information and give context to the request. Two Headers that must be included in any request are the **Host Header** and **Accept Header**. Host Header contains the domain name or IP address of the host. Accept Header to tell the server what kinds of content the client will accept as a response. **If a message body is present**, **Content Length Header** indicates the size of the body in bytes. **Content Type Header** indicates the type of body must be included.
    - **A Blank Line**: after headers. If no message body is required for the request, then the request ends here.
    - **Message Body**: contains the message body,  if it is required for the request. Message bodies might be HTML documents, JSON, encoded parameters, or other similar content.
- **Response** Consists of:
    - **Status-Line**: This includes protocol version and status code, which tell the client the status of the request. There are many possible HTTP status codes. If the request has been successfully processed, the status code of “**200 OK**” will likely show.
    - **Headers**: Like request headers.
    - **A Blank Line**: after headers. If no message body is required for the response, then the response ends here.
    - **Message Body**: Like HTTP request.

**URL-Encoding**

HTTP limits the characters used in URIs, request queries and request bodies to be **ASCII**. Special or unsafe characters, like **space** or **Unicode**, require the encoding of these characters. An example of an unsafe character is a “space” which can be replaced with `%` sign, followed by their two digit hexadecimal digit encoding. For example, a space can be encoded with “**%20**”, or with a “**+**” sign. For example the sentence "software design and architecture" will encoded like:

- software%20design%20and%20architecture
- software+design+and+architecture

And to encoded query string we use `=` symbol to assign each query parameter it's value, 

- color=red
- height=very+tall

and use `&` symbol to join all the parameter value pairs

- color=red&height=very+tall

Now as we said, HTTP request must indicate a request method in it request line. These methods tell web server what if should do with the request. Most request methods usually used are GET, POST, and PUT.

**GET Method**

**GET** methods retrieves the resource given by the URI provided in the request line. For example this could retrieve a webpage, image, or specific output of a program. **A Query String** may be sent along with the request in the URI, it always start with a question mark (?). **No messages body is sent along with a GET request**.

**For example,** you are reviewing a reservation you made on camping.com. At the time of booking, the reservation number 17021 is issued. To review the booking, the url-encoded query string [?number=17021] must be sent to [camping.com/reservation](http://camping.com/reservation).

**Here is the GET Request and Response.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/GET-Method.png" width="500" hight="500"/>
</p>

**POST Method**

is used to add or modify the resource/information according to the message body of the request on the host specified in the URI of the request . HTML forms often use POST requests to submit data.

**For the previous example**. Your family would like to come on the camping trip. You offer to book another campsite for them. As you are creating a new reservation on the website, the POST method will be used for the request.

**Here is the POST Request and Response.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/POST-Method.png" width="500" hight="500"/>
</p>

**PUT Method**

It takes the information provided in the body of the request, and creates or updates a resource at the location specified in the URI of the request. The PUT method can be used to create or update a resource, like the POST method. The information contained in the request body of a POST method, however, is created or updated under an identity and location determined by the web server, which is not necessarily the identity and location in the supplied URI.

**For previous example**, imagine that the camping website allows users to add notes to a reservation, for the staff to receive. Imagine you would like to have a campfire during the trip, but you do not have an axe or wood. The reservation can be accessed with the reservation number. To add a note, a PUT request needs to be made to that location. The note will be a JSON object and delivered in the body of the request.

**Here is the PUT Request and Response.**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/PUT-Method-1.png" width="400" hight="400"/>
  <img src="https://github.com/aboelkassem/Software-and-Service-Oriented-Architecture/blob/main/Images/PUT-Method-2.png" width="400" hight="400"/>
</p>

**HTTP Stateless**

HTTP can also be **stateless**. This means that the relationship between requests is **not preserved**.

For example, if you are browsing an online shopping website and clicking on items. HTTP protocol **doesn't keep track of which items you've previously clicked**. Each time you click another item, a new request is sent, but the protocol is unaware if the same client is making the request.

To **track** the behavior of shoppers on the website, we use **HTTP cookies**, the first time a client makes a request the site gives them an HTTP cookie to store information about the client's browsing session. The cookie is stored by the client (Browser) and updated by the server each time the client makes a request to the server. This allows a server to store state information about interactions with this client, which can be useful for tracking purposes.

HTTP is fundamental for the web, as it dictates how data is communicated and exchanged. This makes HTTP very important for invoking and accessing web services.
