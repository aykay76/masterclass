# Understanding HTTP

**HTTP** stands for **HyperText Transfer Protocol**. It is a way for computers to communicate over the internet. Think of it as a language that web browsers and servers use to talk to each other.

When you type a website address into your browser, HTTP is the protocol that sends your request to the server where the website is hosted. The server then sends back the website content, which your browser displays.

In simple terms, HTTP is like a postal service for the internet, delivering messages between your computer and websites. A similar analogy is to think of the server as a telephone service that has a specific number (the server's IP address and a port number).

Clients (typically a web browser) will connect to a web server on the common port number 80 or 443, although other port numbers can be specified in the URL.

Once connected, the client will send a request to the server. The request is comprised of a request string, a number of optional headers, and an optional body. The request string starts with a verb which tells the server what the client is trying to achieve. Verbs like GET, POST, DELETE will tell the server how to act on the request.

The next part of the request string is URI (universal request identifier) which tells the server which object or entity to perform the request on. In a typical web server the client will typically be requesting resources like web pages, scripts, images and stylesheets. In more advanced systems HTTP can be used as an [API - Application Programming Interface](../API.md) protocol.