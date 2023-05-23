---
title: "Week 07"
date: 2023-03-04
draft: false
author: "Jailani Rahman"
image: /images/blogs/week07.png
description: ""
toc:
---

## First Lesson

**Lesson Date:** 27/02/2023

The objective of this lesson plan was to enable students to identify the tools needed for building web applications using the Spring Framework and to implement a basic response for a Uniform Resource Identifier (URI). The learning objectives for this module were as follows:

Identify the tools needed for building web applications using the Spring Framework.
Able to implement a basic response for a Uniform Resource Identifier (URI).
To achieve these objectives, the lesson plan included the following activities:

During the 2-hour lecture, I explained the required tools for this topic and introduced the concept of web applications. I discussed the purpose of web frameworks and listed different web frameworks for various programming languages. I provided an overview of the Spring Framework and Maven, emphasizing the importance of Maven's dependency management. I guided the students through the process of setting up a Maven project, explained the folder structure, demonstrated how to configure Spring Boot, and introduced the concept of Model-View-Controller (MVC). Additionally, I explained the build setup and demonstrated how to run a Spring web application. I also introduced an alternative method of creating a Maven project using Spring Initializr and showed how to import an existing Maven project.

During the 1-hour practical session, I facilitated the installation of Spring Tool Suite and Maven Repository for the students and guided them through the process of creating a Maven project.

Reflective Evaluation:
I encountered a major issue during the practical session where half of the students' implementations did not work as expected. Despite my efforts, I was unable to resolve the issue within the allotted class time. However, a few students who were experiencing the issue stayed back to seek further assistance during the afternoon session.

To address the issue, I conducted extensive research and attempted various solutions, such as using the @RestController annotation, clearing the Maven repository and re-downloading dependencies, and adding @ComponentScan. After nearly 1 hour and 30 minutes of troubleshooting, I discovered that downgrading the Spring Boot version from 3.0.3 to 2.7.9 resolved the problem. Unfortunately, I was unable to determine the exact cause of the issue with version 3.0.3 and why the request mapping was not properly mapped to the Spring application, resulting in an error. However, using the older version allowed us to proceed with covering the topics in this module.

Moving forward, I will ensure that I thoroughly test and validate the tools and versions used in the practical session to prevent such issues from arising. I will also allocate additional time for troubleshooting in case any unforeseen technical difficulties occur during the implementation phase, ensuring that all students can successfully complete the practical exercises.

---

## Second Lesson

**Lesson Date:** 28/02/2023

The objective of this lesson plan was to enable students to implement the controller and view components of the Spring Framework, as well as gain proficiency in basic Thymeleaf syntax. The learning objectives for this module were as follows:

Able to implement the controller component of the Spring Framework.
Able to implement the view component of the Spring Framework.
Able to implement basic Thymeleaf syntax.
To achieve these objectives, the lesson plan included the following activities:

During the lecture session, I explained why the current application only showed an error page and introduced the concept of Spring Controller. I discussed the differences between Uniform Resource Locator (URL) and Uniform Resource Identifier (URI) and demonstrated how to implement a Spring Controller using examples. I explained the Request Mapping annotation, the ResponseBody annotation, and showed examples of handling URI requests with these annotations. Additionally, I explained how HTML tags can be used in the Controller class and introduced the concepts of Spring View and Thymeleaf. I demonstrated how to create an HTML file and explained how to respond with an HTML file using Thymeleaf. I also covered the integration of static files into a Spring Web Application and explained Thymeleaf URL Expression, Thymeleaf XML Namespace, and different types of URLs.

During the practical session, I facilitated the configuration of Maven projects for the students and guided them in implementing a student management system using the concepts covered in the lecture.

Reflective Evaluation:
I spent 15 minutes ensuring that everyone managed to get their Spring application up and running successfully.

I noticed that only a few students remembered some of the HTML tags from the Basic Web Programming module. To address this, I will make sure to include a recap of the important tags needed in this module to ensure a better understanding of their connection to Spring applications.

Another issue arose when connecting the Spring application with Thymeleaf. It was discovered that Spring Tool Suite excluded the src/main/resources folder from its compilation, resulting in the HTML files not being found by the application. Approximately half of the students experienced this issue. Fortunately, a quick diagnostic and resolution were possible by right-clicking on the src/main/resources folder, selecting "Build Path," and then configuring the inclusions/exclusions filters by removing the "**" from the exclusion filter.

I dedicated 10 minutes to demonstrate the difference between context-relative URLs and server-relative URLs by changing the server.servlet.context-path attribute in the application.properties file to "/myapp".

Overall, the students were able to effectively utilize Thymeleaf and its URL syntax. Moving forward, I will continue to emphasize the importance of understanding HTML tags and their integration with the Spring Framework, and ensure that the issue with Spring Tool Suite excluding the src/main/resources folder is addressed promptly to prevent any hindrance to the students' progress.
