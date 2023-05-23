---
title: "Week 10"
date: 2023-03-25
draft: false
author: "Jailani Rahman"
image: /images/blogs/week10.png
description: ""
toc:
---

## First Session

Lesson Date: 20/03/2023

The objective of this lesson plan was to enable students to implement a data repository in their projects. The learning objectives for this module were as follows:

Able to implement a data repository.
The activities included in this lesson plan were as follows:

During the lecture session, I explained the concept of a data repository and its purpose. I also introduced the use of the @Component annotation and provided an example of a data repository implementation. Furthermore, I explained how to utilize a data repository in the controller, emphasizing the use of the @Autowired annotation. I demonstrated how to pass a list of data to Thymeleaf templates and presented an example of iterating through the list in the templates.

During the practical session, I facilitated the continued implementation of the student management system, building upon the concepts covered in the lecture. This allowed students to apply their understanding of data repositories and further enhance their implementation skills.

Additionally, I scheduled an assignment clinic session, which coincided with the deadline day. The purpose of this session was to ensure that students were able to submit their work on GitHub successfully. I provided support and guidance to address any last-minute issues or challenges faced by the students.

Reflective Evaluation:
During the implementation process, I noticed that some students were confused about how to implement ModelMap. I attributed this confusion to the fact that students had not worked with the code for almost two weeks, as they had been primarily focused on completing the assignment before the deadline. To address this, I emphasized and clarified the usage of ModelMap again to ensure students understood its implementation.

I also realized that some students overlooked the requirement of using the @Autowired annotation for each component declaration. Most students did not declare @Autowired for additional components, which caused Spring to produce an error due to the component not being initialized. I reiterated the importance of using @Autowired for each component and clarified that multiple component declarations require separate @Autowired statements.

Furthermore, some students forgot to include the @Component annotation on their repository class. To reinforce this requirement, I emphasized to the students that when using @Autowired to inject a component, the component class must be declared with the @Component annotation.

Moving forward, I will provide additional examples and hands-on exercises to reinforce the concepts of data repositories and their integration with controllers and Thymeleaf templates. I will also encourage regular coding practice to ensure that students retain their understanding of the concepts and develop proficiency in implementing data repositories.

## Second Session

Lesson Date: 21/03/2023

The objective of this lesson plan was to enable students to generate dynamic pages and handle HTTP requests in their projects. The learning objectives for this module were as follows:

Able to generate dynamic pages.
Able to handle HTTP requests.
The activities included in this lesson plan were as follows:

During the lecture session, I explained the concept of dynamic pages and demonstrated how to generate dynamic URIs. I also covered how controllers handle dynamic URIs and provided an example of a dynamic page. Furthermore, I explained the process of sending data with HTTP requests, including the use of GET and POST methods. I discussed how controllers handle HTTP requests and showcased an example of a controller handling an HTTP request.

During the practical session, I facilitated the continued implementation of the student management system, building upon the concepts covered in the lecture. However, the time allocated for covering dynamic URIs took longer than expected, and we were unable to cover HTTP request handling during this session. I will make sure to address this topic in the upcoming week to ensure students have a comprehensive understanding of handling HTTP requests.

Reflective Evaluation:
While conducting the practical session, I observed that some students were still experiencing difficulties in understanding the process of passing data to HTML files. In order to address this, I spent additional time providing explanations and clarifications on this topic. By doing so, I aimed to ensure that all students had a solid grasp of this fundamental concept before proceeding further.

Based on the challenges faced during the practical session, it became evident that there is a need to cover the topic of HTTP requests more thoroughly. I plan to dedicate ample time in the next session to cover this topic in detail. By doing so, I hope to address any lingering confusion or difficulties that students may have encountered while working on their projects.

Moving forward, I will incorporate more interactive activities and practical exercises to reinforce the concepts of dynamic page generation and HTTP request handling. These activities will allow students to apply their knowledge in a hands-on manner, further solidifying their understanding of the concepts. Additionally, I will closely monitor student progress and provide timely support to address any challenges they may encounter.
