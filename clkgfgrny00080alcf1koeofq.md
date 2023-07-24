---
title: "Anatomy of an API Response"
seoTitle: "Decoding API Responses: Unveiling the Core Components""
seoDescription: "Unraveling the core of API responses for efficient data exchange and seamless communication in software development"
datePublished: Mon Jul 24 2023 05:28:48 GMT+0000 (Coordinated Universal Time)
cuid: clkgfgrny00080alcf1koeofq
slug: anatomy-of-an-api-response
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690175877884/5218bb7c-4bb6-4070-9d09-8b49fd9eace6.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1690176240611/b0e0b8a0-4765-490f-9b4c-84ba6f906736.png
tags: software-development, backend, apis

---

### Introduction

In the last article on [*Anatomy of an API Request*](https://codedaddy.hashnode.dev/anatomy-of-an-api-request)*,* We saw how APIs can send requests in order to receive a response. In the world of modern web development and software architecture, APIs play a crucial role in facilitating seamless communications between client applications and servers. APIs allow developers to interact with remote services, access valuable data, or perform specific actions in a standardized and efficient manner. When a client sends an API request to a server, it expects to receive a well-structured and informative response in return. Understanding the "Anatomy of an API Response" is fundamental for developers working with APIs, as it forms the basis for effective data retrieval and application functionality.

### What is an API Response?

An API response, also known as an API (Application Programming Interface) response, is the data that a server sends back to a client after the client makes a request to the API. From our last interactions on this subject matter, we can see that as long as a request is sent, a response is always sent back. There are about four components that make up an API response, which are:

* *Response body*
    
* *Status codes*
    
* *Response headers*
    
* Response Links
    

These are the major components that make up an API response. Though all are not compulsory, it is vital that you always have your response body and your status code, depending on what type of request you are making.

1. #### Response Body
    

The response message contains the message we would like the server to return to the client. The message can be sent in any format you want, either in JSON format, text, a file, or any other format.

A typical response body looks like this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690019858228/8f4208dc-ca3c-4595-b6dd-0ed781c89ab4.png align="center")

This is a login response, which returns the information above to the client. The example above shows that the server response is in JSON format. To understand more about JSON, check out this article by [**Prakash Kumar**](https://hashnode.com/@PrakashK) on [*Unlocking the Power of JSON: Simplifying Data Exchange in Web Development*](https://prakashraj.hashnode.dev/unlocking-the-power-of-json-simplifying-data-exchange-in-web-development)*.*

1. #### HTTP Status Codes
    

HTTP status codes are three-digit numeric codes that indicate the outcome of an HTTP request-response cycle. The status code tells us the status of our response from the server and helps the client understand whether the request was successful, encountered an error, or requires further action.

> The [Internet Assigned Numbers Authority](https://en.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority) (IANA) maintains the official registry of HTTP status codes

We have about five categories of status codes, which include:

* ***1XX*** *\- Informational Response:* This indicates that the request was delivered successfully to the server. One of the popular status codes used in this series is the `101` which is the switching response status code. Used in Web sockets to switch from the HTTP protocol to the Web Socket protocol.
    
* ***2XX*** *\- Success:* This response code tells the client that the request was received and was successful. Some of the popular response codes used in this series include:
    
    * `200` - `OK` tells us that the response was successfully processed.
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690026409072/ae4adfd8-2aa8-492d-8bfc-3593d7c289d1.png align="center")
    
    * `201` - `CREATED` tells us that the request to create a new resource was executed successfully.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690026754139/60444eb0-3138-4493-822e-7f9b324455fe.png align="center")
        
    * `204` - `NO CONTENT` tells us that the request was executed successfully but is returning no response body from the server.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690027632187/51a23895-7289-4107-8b2e-7baccf4f0769.png align="center")
        
* **3XX -** *Redirection:* Tells the client to take additional action to complete his/her request. Personally, I have not used this status code.
    
* ***4XX*** *\- Client Error:* This status code tells us that the error encountered by the server was caused by the client. Some of the popular status codes that are used are the
    
    * `400` - `BAD REQUEST` This status code tells us that there is a problem with the incoming message, it could be too large, invalid format, and many more.
        
    * `401` - `UNAUTHORIZED`, this means that the client must be authenticated/recognized before accessing that resource. There are different authentication methods. Some of them include:
        
        * API Keys
            
        * Basic Auth
            
        * Bearer Token
            
        * JWT Bearer
            
        * OAuth
            
        
        A typical example of this is when accessing some resource when you are not logged in. Many times in backend applications, the client is given a token to always use when communicating with the server. This token is usually passed in the header using the bearer token.
        
        ````markdown
        ```'Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiI2NGJiY
        WE4ZjIwZWY3ZDAwNDIzZjc5YmMiLCJpYXQiOjE2OTAwMjY5NzMsImV4cCI6MTY5
        MjYxODk3MywidHlwZSI6InJlZnJlc2gifQ.CiIodT7rT6gUhe3lNblScAujF92F
        992nI0d5FYVfu-Y'```
        ````
        
        This token is received by the server and decoded to authenticate the user, and if the user is valid, the user is allowed to access the resource.
        
        Here is a typical example of trying to access a resource that we cannot:
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690018541403/1c59b805-ab96-4915-a136-c72b01b0c533.png align="center")
        

That is the server telling me that I am not authenticated to access the resource.

* `403` - `FORBIDDEN`. This status code is similar to `401`, the only difference is that the user is forbidden to access that resource as the client has no right to access that resource. This does not mean that the client is not authenticated, the client is but is not authorized to access that resource. A good example is between an admin and a user. An admin can fetch other users and their details, but a user can only fetch himself and details relating to himself only. Here is an example response:
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690021104903/07cbf0a0-6856-4a92-8bad-f065376a2766.png align="center")

* `404` - `NOT FOUND` This response code tells us that the endpoint, page, or resource we are trying to access does not exist. Here is an example response:
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690023996670/a99e747c-b0b1-4d44-abd3-1722d8095bed.png align="center")

### Response Headers

Similar to the API request, the API response can also include headers that provide additional information about the response or the server. Common headers include:

* **Content-Type**: Specifies the format of the data being returned (e.g., JSON, XML).
    
* **Content-Length**: Indicates the length of the response data in bytes.
    
* **Cache-Control**: Specifies caching directives for the response.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690025301392/46266e91-ae3a-412d-b352-2523bd9f2186.png align="center")

This whole information comes in the header of the response, as it helps us in many ways. Here are some possible ways it can help us

1. **Metadata and Information:** Response headers provide additional metadata and information about the response data. For example, the "Content-Type" header indicates the format of the data in the response (e.g., JSON, XML, HTML). This helps clients understand how to parse and process the response data correctly.
    
2. **Caching and Performance Optimization:** Headers like "Cache-Control" and "Expires" allow servers to specify caching directives for the response. Clients can cache the response data locally, reducing the need to make redundant requests to the server. This improves performance and reduces server load, benefiting both clients and servers.
    
3. **Authentication and Security:** Headers such as "Authorization" are essential for authentication and security purposes. They allow servers to enforce access control rules, ensuring that only authorized clients can access specific resources. This helps protect sensitive data and restrict unauthorized access.
    
4. **Cross-Origin Resource Sharing (CORS):** The "Access-Control-Allow-Origin" header is used in CORS to specify which origins (domains) are allowed to make requests to the server. This header helps prevent cross-origin security issues and enables controlled access to resources from different domains.
    
5. **Compression and Content-Encoding:** Response headers like "Content-Encoding" inform clients about compression techniques applied to the response data. This allows clients to decompress the data appropriately, reducing bandwidth usage and improving load times.
    
6. **Redirect Handling:** Headers like "Location" are used for redirection. When a resource has moved or needs to be accessed via a different URL, the server can send a redirection response, guiding the client to the new location.
    
7. **Error Handling and Debugging:** Response headers often contain information about errors or exceptions that occurred during the request's processing. The "X-Request-ID" or "X-Correlation-ID" headers are sometimes used to facilitate debugging and tracing of requests across distributed systems.
    
8. **Versioning and API Changes:** API response headers can include information about the API version or any deprecation warnings. This helps clients understand the API's compatibility and anticipate any changes or deprecations.
    

### References

List of HTTP status codes. (2023, July 18). In *Wikipedia*. [https://en.wikipedia.org/wiki/List\_of\_HTTP\_status\_codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)