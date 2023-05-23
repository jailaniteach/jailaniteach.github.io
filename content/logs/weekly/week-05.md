---
title: "Week 05"
date: 2023-02-18
draft: false
author: "Jailani Rahman"
image: /images/blogs/week05.png
description: ""
toc:
---

## First Session

**Lesson Date:** 13/02/2023

The focus of this lesson plan was to help students understand the concept of a client-server application and enable them to implement basic client-server applications. The learning objectives for this module were as follows:

Understand the concept of a client-server application.
Understand and be able to implement a basic client-server application.
To achieve these objectives, the lesson plan included the following activities:

During the 1-hour lecture, I reviewed the Internet Protocol and introduced the concept of a client-server architecture. I explained the typical process involved in network programming and provided detailed explanations on Java's ServerSocket and Socket objects. I discussed the connection process between server and client sockets, data transmission through sockets, and how to obtain InputStream and OutputStream objects from a Socket. Additionally, I demonstrated how to wrap these objects using DataInputStream and DataOutputStream. I presented an example of a client-server application for calculating the area of a circle and addressed exceptions such as ConnectException and BindException. I also covered topics such as handling port numbers with ServerSocket and Socket, using the InetAddress object, identifying host name IP, handling multiple clients, threads, multithreading, Java tasks, and Java threads. I concluded the lecture with an example of a server that can handle multiple clients and explained the process of sending and receiving objects. Finally, I demonstrated a client-server application that transmitted objects.

During the 2-hour practical session, students were provided with hands-on experience in implementing various client-server applications. They were guided through the implementation of a client-server application for calculating the area of a circle, a client-server application for calculating the area of a rectangle, and a server application capable of handling multiple clients.

Reflective Evaluation:
During the lecture, I noticed that some students struggled to understand the example where both the server and client applications were receiving and sending data simultaneously. To address this confusion, I decided to modify the practical examples by focusing the server application on receiving data and the client application on sending data. This adjustment helped clarify the concept for the students and improve their understanding.

However, during the implementation of the server application that handled multiple clients, I encountered some challenges. My original plan was to introduce another class to demonstrate the implementation, copying the relevant code from the previous server application and placing it within a thread. Unfortunately, this approach caused confusion among the students regarding the placement of specific code segments. As a result, I spent more time than anticipated explaining the implementation process. In hindsight, I should have manually implemented certain parts while utilizing copy-paste for other segments to prevent confusion and streamline the learning experience.

Overall, the lesson plan effectively achieved the learning objectives of understanding client-server applications and implementing basic client-server functionality. Reflecting on the session, I recognize the importance of adapting examples and exercises to address students' comprehension challenges. Additionally, I have learned that a careful approach to code organization and implementation demonstration can significantly impact students' understanding and reduce confusion during practical sessions. By making these adjustments, I aim to enhance the effectiveness of future lessons on client-server applications.


## Second Session

**Lesson Date:** 14/02/2023

The focus of this lesson plan was to enable students to understand and implement a basic client-server application. The learning objective for this module was as follows:

Understand and be able to implement a basic client-server application.
To achieve this objective, the lesson plan included the following activities:

During the 1-hour 30-minute practical session, I facilitated the implementation of a client-server application for calculating the area of a circle. I instructed the students to create a new package, "week02.slot02," and move previously created classes that were not used in the previous session to this new package. I guided them in creating the CircleSessionHandler class and implementing the server application to allow client connections. I then assisted in the implementation of the server application to receive radius inputs from clients and send the calculated area back to the client. Additionally, I helped students develop the functionality to handle multiple clients simultaneously. Students were also guided in implementing the client application to connect to the server, send the radius to the server, and receive the area in response. Time was allocated for testing the implementation to ensure its proper functionality.

During the 1-hour 30-minute exercise session, students were tasked with implementing a server-client number guessing game. The basic requirements included the server generating a random number from 1 to 100, and the client needing to guess the number until answered correctly. The server would provide feedback to the client, indicating if the guess was higher or lower than the generated number. Both the client and server applications would terminate after the client guessed correctly. For advanced requirements, a two-player guessing game was introduced. The server would match two clients in a session based on a first-come, first-serve basis, generate a random number, and both clients would need to guess the generated number. The server would inform each client if their guess was higher or lower, and the session would terminate after a client guessed correctly, with the winner being announced.

Reflective Evaluation:
During the practical session, I focused on implementing best practices, which resulted in me not allowing students to run the application periodically. It wasn't until after an hour of coding that I realized the importance of letting students run and see the results of their implementation throughout the process. In the future, I will re-evaluate the step-by-step implementation approach to allow for periodic running of the application. I may consider omitting certain elements, such as try-catch statements, as the students have already learned this concept during the introduction to programming and object-oriented programming modules.

During the exercise session, I noticed that some students struggled with approaching the problem. It became apparent that some of them had forgotten the basics of client-server applications. This highlighted the need for more practice to solidify their understanding of the client-server concept and to refresh their knowledge from the introduction to programming and object-oriented programming modules.

Based on these observations, I will incorporate additional exercises and examples in future sessions to reinforce the fundamental concepts and ensure that students have a solid grasp of client-server application development. By providing more opportunities for practice and revisiting essential topics, I aim to enhance students' understanding and confidence in implementing basic client-server applications.
