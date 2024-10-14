# What is an API?

## Introduction
An API, or Application Programming Interface, is a way for different software applications to communicate with each other. Think of it as a translator that helps two different systems understand each other. One application could be written in one language and the other application written in a different language - an API allows them to communicate with a common language, or protocol, most commonly [HTTP - the Hypertext Transfer Protocol](../Protocols/HTTP.md).

While HTTP was initially developed for transferring web pages it has become a general medium transfer protocol. Other protocols have been developed which are more efficient over the wire (air) like gRPC.

APIs are a common integration pattern for large enterprises where multiple teams are working on different pieces of software that will need to communicate with each other. This approach allows different teams to focus on different parts of a larger system, then come together to agree the interface, or contract, that will allow the parts to communicate.

Due to the fact that APIs have evolved along with HTTP they typically take the form of a request/response interaction. The 'client' will connect to a server and make a request, the server will process the request and return a response. The content of the request and response are typically in JSON (Javascript Object Notation) format - another format that has evolved with the web.

**_NOTE:_**  There are other integration pattern such as EDI (Electronic Data Interchange), messaging, event passing and others.

## REST (Representational State Transfer)

While APIs can be any form of request/response interaction, they are typically used to pass the state of a business object from one service to another. This approach has come out of DDD (domain driven design) where each domain contains particular objects - for example, an inventory system will contain information about SKUs, a CRM system will contain information about a customer and a billing system will contain information about accounts.

An API allows systems to perform 'CRUD' operations on objects without directly accessing another system's database. Here CRUD stands for Create, Retrieve, Update and Delete. The operations are mapped onto HTTP verbs:

CRUD Operation|HTTP Verb(s)
-|-
Create|POST
Retrieve|GET
Update|PUT, PATCH
Delete|DELETE

## Everyday Examples
Imagine you are at a restaurant. You (the user) look at the menu (the application) and decide what you want. You then tell the waiter (the API) your order. The waiter takes your order to the kitchen (the server), where the food is prepared. Finally, the waiter brings your food back to you. In this analogy:
- **You** are the user.
- **The menu** is the application.
- **The waiter** is the API.
- **The kitchen** is the server.

## Considerations
There are some additional consideration to take into account when developing APIs:

### Hosting
Whether your API is intended for internal use only, or if you intend to make it available to users all over the internet, you will need to host your API somewhere so that it can be connected to by clients. It could be as simple as running the API on your computer to connect different pieces of software locally, or it may be hosted in the cloud and accessible over the internet. (The latter approach introduces additional considerations discussed below).

### Performance
Response times for APIs are important - nobody likes to wait for a response when they have asked for something, especially in the modern world. There are different aspects of your API that will potentially affect response times:
- number of concurrent calls
- hosting platform
- complexity of serving software

### Security 
By definition, APIs open up your software to communication from outside its own boundary. This introduces complexity especially when it comes to security. I mentioned HTTP above but to add an extra layer of security you should secure the API endpoint with TLS (Transport Layer Security) which requires a certificate.

Will you let just anyone call your API or do you want some form of authentication in place?

### Version Control
It's important to have good version control over your APIs. Imagine you are developing an API for others to consume and one day you decide to make a change that means the contract is no longer valid. If you had thousands of clients calling your API, they could all cease to function correctly causing issues of stability, reputational damage and potentially cost (if the API is monetised).

### Discoverability
How do others know your API exists? And how do they know which authentication mechanism to use? Larger organisations will typically have some form of API catalogue where teams can publish their API contracts and details about how to use the API.

## Conclusion
APIs are essential tools in modern software development. They allow different applications to communicate and share data, making it easier to create complex systems.
