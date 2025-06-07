# Multithreaded-Chat-Application

The objective of Task 3 is to design and implement a multithreaded chat application using Java sockets. This application facilitates real-time communication between multiple clients and a central server. By leveraging multithreading, the server can handle multiple clients simultaneously, ensuring smooth and concurrent interactions without blocking any individual connection.

At its core, a chat application allows users to send and receive messages. In a multithreaded environment, each client that connects to the server is managed by its own thread. This means that messages from different clients can be received, processed, and broadcasted in real time without delay. Java provides the necessary tools for creating sockets, which act as endpoints for sending and receiving data over a network, and threads for managing multiple processes simultaneously.

The application consists of two main components: the server and the client. The server is a continuously running program that listens for client connection requests on a specific port. When a client connects, the server creates a new thread dedicated to handling communication with that client. This thread listens for messages from the client and, upon receiving a message, relays it to all other connected clients. This broadcast mechanism is central to the chat application’s real-time capability.

On the client side, the program connects to the server using its IP address and port number. Each client has a simple interface where the user can input messages. The client listens for incoming messages from the server in a separate thread to avoid blocking the user input. When a user sends a message, it is transmitted to the server, which then broadcasts it to all connected users, creating a group chat effect.

The use of multithreading is crucial in this application. Without it, the server would only be able to handle one client at a time, which defeats the purpose of a chatroom. Each thread runs independently, allowing multiple clients to send and receive messages without interfering with one another.

This project provides a solid introduction to network programming, multithreading, and inter-process communication in Java. It demonstrates how sockets can be used to create reliable client-server architectures and how threads can enhance responsiveness and scalability. Students learn to manage shared resources safely, handle exceptions in network communication, and implement graceful disconnection of clients.

For testing and demonstration, at least two client instances should be run on the same or different machines (on the same network or using localhost). Each client should be able to send a message and receive messages from other connected clients, confirming the successful functioning of the chat application.

Overall, this task builds essential programming skills in concurrency and network programming. It also introduces the fundamentals required for developing more complex systems such as multiplayer games, collaborative platforms, and messaging apps. By completing this task, interns gain hands-on experience in building a real-time communication tool, preparing them for more advanced distributed systems and backend service development.
