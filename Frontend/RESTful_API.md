# RESTful API

## What is RESTful API?
 - A RESTful API (Representational State Transfer Application Programming Interface) is a type of web service that follows the principles and constraints of the REST architectural style. 
REST is an architectural style for designing networked applications, and RESTful APIs provide a standardized way for different software applications to communicate with each other over the internet.

## Some key principles of a RESTful API:  

**Statelessness:** Each request from a client to the server must contain all the information needed to understand and process the request. 
The server should not store any client state between requests. Each request should be independent and self-contained.  

**Client-Server Architecture:** RESTful APIs adhere to a client-server model, where the client and server are separate entities. 
The client is responsible for the user interface and user experience, while the server is responsible for processing requests and managing resources.  

**Resource-Based:** Resources are the key concept in a RESTful API. A resource can be any object, data, or service that the client wants to access. 
Each resource is identified by a unique URL (Uniform Resource Locator).  

**CRUD Operations:** RESTful APIs use standard HTTP methods to perform operations on resources:  
 - GET: Retrieve a representation of a resource.
 - POST: Create a new resource.
 - PUT: Update an existing resource or create a new one if it doesn't exist.
 - DELETE: Remove a resource.  

**Uniform Interface:** RESTful APIs have a uniform and consistent way of interacting with resources, using standard methods and HTTP status codes. This simplifies the API design and makes it easier to understand and use.  

**Representation:** Resources are represented in a format such as JSON (JavaScript Object Notation) or XML 
(eXtensible Markup Language) to enable data exchange between the client and server.
