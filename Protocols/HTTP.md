# Understanding HTTP

**HTTP** stands for **HyperText Transfer Protocol**. It is a way for computers to communicate over the internet. Think of it as a language that web browsers and servers use to talk to each other.

When you type a website address into your browser, HTTP is the protocol that sends your request to the server where the website is hosted. The server then sends back the website content, which your browser displays.

In simple terms, HTTP is like a postal service for the internet, delivering messages between your computer and websites. A similar analogy is to think of the server as a telephone service that has a specific number (the server's IP address and a port number).

Every computer on the internet (or a local network) has an internet protocol address (IP Address) that uniquely identifies it. Within a server there may be multiple pieces of software running so how does a client know which one to connect to? Each service 'listens' on a particular port so that clients know where to connect.

Some common port numbers:

Port|Service
-|-
80|HTTP (web)
443|HTTPS (secure web)
25|SMTP (email)
21|FTP (file transfer)
