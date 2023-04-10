# Full stack developer Roadmap 2023 :

## Browsers :

- Learn about how browsers are made, browser apis, etc.

## Communication Protocols :

- It is a protocol which computer systems need to follow when they need to communicate which each other.
- A protocol is a set of defined rules.
- There are 2 important types of protocols.

### Transport Layer protocols : TCP and UDP

- Get a high level overview of this topics
- In TCP, when machine A tries talking with another machine B and there is a network discrepancy, the machine A will keep sending messages until it is able to create a connection. Eg: Instagram login
- In UDP, machine A will just keep throwing messages/packets to machine B and if machine B dosen't accepts it, there is no acknowledgement from the server to tell that he machine B has received message. Eg: Live streaming, Zoom call where we miss some parts of the video still it's not a big problem.

### Application Layer protocols : HTTP

- Communication protocol used by browsers to interact with servers.
- HW- Write HTTP server in C++

## Databases :

- Learn to store any type of user data.

## Messaging Buses or Pub subs :

- Using above things we can build basic fullstack apps with authentication. But when we want to build complex apps such as instagram where on login from a different device you get notified on your mail that is the new login made by you, we need Asynchronous Communication like Message buses.
- Like when we perform a UPI transaction, we get the message from bank after 5-6 seconds about the money been debited. So we understand that message from bank is not an important event but it is required to be performed and a Successful transaction is more important as the feedback needs to be shown on the app.
- So we offload such tasks which need to reach user but not immediately through other backend processes.

### Workflow :

- Font end sends a request to backend server.
- Now backend sends request to Email/message server which has the responsibility of emailing/text messaging the user.
- We didn't use the same backend server to perform above tasks as that server is required to serve immediate important requests.
- since the backend sends an HTTP request to email server, it will wait until it receives response. In case the email server is down, our backend will keep waiting.
- To avoid such cases, Messaging buses are used. It is basically a server which sits between backend and email server and has a queue in it. Backend puts the message into that queue and then email server can keep picking up each msg from it. So whenever the email server comes back up, it can pick up the request message from queue and send email accordingly with the delay.
- This is a type of MicroServices architecture.






















