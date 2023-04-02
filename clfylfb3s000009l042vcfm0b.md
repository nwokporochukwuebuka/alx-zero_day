---
title: "API 101: A Beginner's Guide to Application Programming Interfaces (Part One)"
seoTitle: "A Beginner's Guide to APIs (Part One)"
seoDescription: "Start with this beginner's guide to APIs, covering definitions, types, architectures, endpoints, requests, and responses"
datePublished: Sat Apr 01 2023 23:16:57 GMT+0000 (Coordinated Universal Time)
cuid: clfylfb3s000009l042vcfm0b
slug: api-101-a-beginners-guide-to-application-programming-interfaces-part-one
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680459484783/d5aba4d2-01da-4012-999c-142283c4ec5e.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680390827689/711c2f68-90aa-4549-9251-2f81c1a1d2fd.png
tags: web-development, apis, architecture, programming-ciovqvfcb008mb253jrczo9ye, web-services

---

### Definition of an API

Have you ever wondered how the Internet works? We have probably heard that the internet consists of interconnected servers. These interconnected servers must communicate to share resources among themselves. For example, when we type *www.hashnode.com* on our web browser, a request is made to a server somewhere, and resources are immediately gotten and displayed on the web browser.

An **API** is what makes this possible.

**API** is an acronym that stands for **Application Programming Interface**. An API is a set of protocols, routines, and tools that allow different software applications to communicate with each other.

When a client wants to use data or functionality provided by a web service, it can use the API provided by that service to request the information it needs. The API acts as an intermediary, translating the client's request into a format the web service can understand, and then processing the response back into a format the client application can understand.

Overall, APIs are a critical component of how the internet works, enabling different software applications to work together and providing new and innovative resources to users.

---

### Why APIs are important for businesses

* APIs allow developers to work together effectively. Hence, it increases productivity.
    
* APIs also allow businesses to manage their data more effectively by providing a secure, scalable, and standardized way to access and share data between different applications and systems.
    
* APIs can be used to monetize data and services, providing a new source of revenue for businesses.
    
* APIs also speed up the development process by allowing developers to access pre-built functionality and services, reducing the time and effort required to build new applications.
    
* APIs also add additional security to our applications. Security is strengthened by tokens, signatures, gateways, etc.
    

---

### Types of APIs

* **Open APIs:** They are also known as *public APIs*, they are APIs that are available to anyone because they have minimal restrictions.
    
* **Internal APIs:** These *APIs* are also known as *private APIs* and are usually designed for use within an organization or company. They are used by various departments to share and access resources and services.
    
* **Partner APIs:** These *APIs* are designed for use by strategic partners or third-party companies. They are often used to provide additional functionality to existing products.
    
* **Composite APIs:** These *APIs* combine multiple APIs. They allow developers to access data and functionality across multiple sources through a single API.
    

### API Architectures

APIs help us exchange data, and for this to be possible, there are a set of rules or protocols that are in place that govern the functioning of APIs.

API architecture refers to the architectural ideas and patterns that are used to develop and structure an API.

Here are some API architectures that are commonly used:

#### **SOAP (Simple Object Access Protocol):**

This type of architecture was developed by the World Wide Web Consortium. A SOAP message is an XML-based message that is used to exchange data between applications over a network.

##### **Features of SOAP**

SOAP messages are made of four blocks, which are *the header, envelope, body, and fault.*

* **Envelope**: This is the first element of a SOAP message. It helps to separate it from other XML documents. So it provides a standard structure for encoding the message.
    
* **Header**: It is an optional part of the SOAP message. It can also contain the authentication or encryption message for a particular request.
    
* **Body:** This is the part that carries the actual data we are transmitting.
    
* **Fault:** This part is used to report errors whenever there is an error. It is enveloped inside the *body* block.
    

As a result, a SOAP remote procedure call (RPC) request or answer comprises delivering data in XML format to a SOAP server, and the server responds in XML format.

#### REST (Representational State Transfer)

It is also called "RESTful APIs." This architecture is the most popular among industries because of its flexibility. REST APIs are based on the HTTP protocol and use the HTTP verbs (GET, POST, PUT, PATCH, DELETE, OPTIONS, TRACE, HEAD, CONNECT) to perform operations on resources. For REST services, requests and responses are usually in JSON (JavaScript Object Notation) or XML (Extensible Markup Language)

To build RESTful APIs, there are design principles that you must follow, which are:

1. **Stateless**: The server does not keep any client context and each request from a client to it provides all the information required to fulfill the request.
    
2. **Client-Server**: More flexibility and scalability are possible because of the distinct separation of the client and server.
    
3. **Universal Interface**: A consistent interface makes the design simpler and enables client-server decoupling.
    
4. **Cacheable**: For faster performance, RESTful API responses may be cached.
    
5. **Layered System**: A layered system makes the design more scalable and straightforward.
    

You can also check out [**Adelani A-Adele**](https://hashnode.com/@AdelaniAA)**'s** blog on "[What are REST APIs?](https://adelaniaa.hashnode.dev/what-are-rest-apis)"

REST APIs consist of the following components:

1. **Base URI(Uniform Resource Identifier):** This is the starting point of a REST API and is used to identify the API and its version. It is sometimes called the "base URL" or "entry point" of the API.
    
2. **Resources:** These are the data entities that are exposed by the APIs. Each resource is identified by a unique URI and can be accessed using the appropriate HTTP method (GET, POST, PUT, DELETE, etc).
    

#### GRAPHQL

This is a new type of API that allows clients to specify exactly what data they need, and only receive that data in response. GRAPHQL APIs use a single endpoint to retrieve data, and clients can specify the fields, relationships, and filters they want to query. They can help reduce the amount of data transferred over a network, which can in turn improve performance and flexibility.

A GRAPHQL API typically consists of the following components:

* **Schema:** This defines the type of data that can be queried and the operations that can be performed on that data.
    
* **Queries:** This is used to fetch data from the GRAPHQL API. These queries are written in GRAPHQL language, and they specify the data that the data want to retrieve from the server.
    
* **Mutations:** They are used to modify data on the server.
    
* **Subscriptions:** They are used to establish a persistent connection between the client and the server, and to receive real-time updates as the data changes on the server.
    
* **Resolvers:** They are responsible for resolving queries and mutations in the GRAPHQL API.
    
* **Middlewares:** This is the code that is executed before or after a resolver function is called. It can be used for a similar purpose as used in REST architecture.
    
    Other components include the client and the data sources.
    

### API Endpoints and Requests

#### Endpoints

When we build APIs, in order for them to be accessed, we create links that enable other resources to locate them. Endpoints are like entry points to access the server.

We can therefore say that an endpoint is a location from which APIs can access the resources they need to carry out their function.

For example, here is an endpoint for retrieving the number of books registered on a website `https://api.example.com/books`

#### HTTP Methods

Endpoints tell us how to locate APIs and resources, but this is not enough to carry out the actions that we need to. HTTP (HyperText Transfer Protocol) is a protocol or set of rules that is used for transferring data over the web. This set of rules is what we call the HTTP methods, or verbs. They indicate what type of action should be performed. Here is a list of HTTP methods and their meaning:

1. **GET**: This method is used to retrieve data or resources from a specified server using a URL. It should only be used to retrieve data and not to modify or delete it.
    
2. **POST**: This method is used to submit data to be processed by a specified resource on the server. It is commonly used for creating new resources, such as submitting a form or creating a new user account.
    
3. **PUT**: This method is used to update or replace an existing resource on the server with a new one.
    
4. **DELETE**: This method is used to delete a specified resource on the server.
    
5. **PATCH**: This method is used to update a specific part of an existing resource on the server.
    
6. **HEAD**: This method is similar to GET, but it only retrieves the header information for a specified resource without returning the actual data.
    
7. **OPTIONS**: This method is used to retrieve the available HTTP methods and other options for a specified resource.
    
8. **CONNECT**: This method is used to establish a network connection to a specified resource.
    
9. **TRACE**: This method is used to retrieve a diagnostic trace of the HTTP request and response messages for a specified resource.
    

#### Requests and Responses

Requests refer to the message sent by a client application to the API using the HTTP verbs. The request typically includes information such as the HTTP method (e.g., GET, POST, PUT, DELETE, etc.), the endpoint URL, and any additional data required by the API. Like the previous example, we said that to retrieve the list of books registered on a website, we use the endpoint described and send a GET method, i.e., `GET https://api.example.com/books`. This request is sent to the server to fetch a list of all the books on the platform.

After receiving a request, the API processes the request and returns a response to the client application. The response typically includes the requested data or a confirmation of the successful execution of the requested operation. It may also include additional metadata, such as response headers and status codes, to provide additional context about the response.

You can follow me on the following platforms so as to get a notification when part two drops:

Twitter 🐦: @[@nwokporo_ebuka](@nwokporo_ebuka)

LinkedIn ⚡: @[@chukwuebuka_nwokporo](@chukwuebuka_nwokporo)

GitHub 🚀: @[@ebukvick](@ebukvick)

Hashnode 📗: @[Nwokporo Chukwuebuka](@codeDaddy)