---
title: Week 04
date: 2023-02-11
description: Teaching log for Week 04
draft: false
hideToc: false
enableToc: true
enableTocContent: true
author: Jailani Rahman
authorEmoji: 💻
---

# First Session

**Lesson Date:** 06/02/2023

I successfully implemented a lesson plan focused on reviewing the TCP/IP network layer and introducing Java binary input and output. The learning objectives of this module were as follows:

Review the concepts of the TCP/IP network layer.
Understand and apply Java binary input and output in the context of network programming.
To achieve these objectives, the lesson plan included the following activities:

During the lecture on "Introduction to Network Programming," which lasted for 1 hour, I reviewed the fundamental concepts related to networks. This included a comprehensive review of each component in the layers of the TCP/IP network, including Internet Protocol (IP), Transmission Control Protocol (TCP), User Datagram Protocol (UDP), IP addresses, Domain Name System (DNS), ports, the internet, internet address blocks, network address translation, firewalls, and proxy servers.

In the subsequent lecture on "Java Binary Input & Output," which lasted for 30 minutes, I provided a review of Java input-output operations in general and introduced the specific context of network programming. I explained the difference between Java text and binary input-output, presented the inheritance tree of the Java binary input-output library, and detailed the methods available in InputStream and OutputStream. I also provided a comprehensive explanation of how to use FileInputStream and FileOutputStream, emphasizing proper stream closing techniques using traditional try and catch statements and the more efficient try-with-resources approach.

To assess students' understanding, a 15-minute quiz was administered through the PBLMS platform, focusing on Git remote operations.

During the practical session on "Java Binary Input & Output," which lasted for 1 hour and 15 minutes, I facilitated students in revisiting the implementation of Java text input-output operations. I then guided them through the process of implementing basic Java binary input-output operations. During this session, I highlighted the differences between the two approaches and demonstrated the usage of FileInputStream and FileOutputStream.

Reflective Evaluation:
The recap of the basic concepts of networks proceeded smoothly without any issues. However, I plan to emphasize certain important concepts related to the practical session in the upcoming week to ensure a better understanding among the students.

During both the lecture and practical session, I engaged students by posing questions to assess their retention of concepts covered in previous Java modules. As anticipated, only a few students were able to provide accurate answers. This highlights the need to revisit concepts that have not been recently addressed, as it takes time for students to recall information that has not been actively reinforced. In response to this, I briefly recapped important concepts such as object creation, class and instance variables, try and catch statements, and implementing repetitive tasks. This recapitulation served to reinforce their understanding of these concepts as well.

Overall, the lesson plan effectively achieved the learning objectives of reviewing the TCP/IP network layer and introducing Java binary input and output. Reflecting on the session, I will continue to reinforce previous Java concepts and ensure students have a solid foundation before progressing further.

---

# Second session

**Lesson Date:** 07/02/2023

Throughout this lesson plan, my aim as an educator was to ensure that students gain a comprehensive understanding of Java binary input and output and are able to apply it effectively. The learning objective for this module was as follows:

Understand and apply Java binary input and output.
To achieve this objective, the lesson plan included the following activities:

During the 30-minute lecture, I provided detailed explanations on how to use DataInputStream and DataOutputStream, BufferedInputStream and BufferedOutputStream, and ObjectInputStream and ObjectOutputStream. I emphasized the significance of implementing the Serializable interface for object storage and delved into the purpose of the Serializable interface.

The practical session, which lasted for 1 hour and 30 minutes, focused on facilitating students in using the different input and output streams discussed in the lecture. I guided them through the usage of DataInputStream and DataOutputStream, BufferedInputStream and BufferedOutputStream, and ObjectInputStream and ObjectOutputStream. Additionally, I highlighted the fact that an object cannot be stored if its class does not implement the Serializable interface.

During the practical exercise, which spanned 1 hour, students were required to implement a Java application to create a copy of a file. I provided guidance and support as they worked on the exercise.

Reflective Evaluation:
During the lecture, I dedicated an additional 15 minutes to explain how objects are stored in computer memory. This served to emphasize the reason why Java does not duplicate objects when storing them into a file using ObjectOutputStream. This extra clarification helped students gain a deeper understanding of the underlying concepts.

At the start of the practical exercise, I had to guide the students on connecting their Java projects to GitHub once again. It was apparent that some students had forgotten the steps since a week had passed since the initial instruction. I allocated 10 minutes to guide them through the process. It is crucial to recognize that without regular practice, students may forget certain steps or concepts. To accommodate students who were unable to complete the exercise by the end of the class, I requested that they finish it at home and upload their project to GitHub.

Overall, the lesson plan effectively achieved the learning objective of understanding and applying Java binary input and output. Reflecting on the session, I acknowledge the importance of reinforcing key concepts and procedures when students have had a significant time gap since the initial instruction. By providing additional explanations and offering guidance during the practical exercises, I aimed to foster a stronger grasp of the material and facilitate a more successful learning experience.
