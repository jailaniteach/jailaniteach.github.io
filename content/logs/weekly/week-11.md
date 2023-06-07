---
title: "Teaching Practice Week 11"
date: 2023-04-01
draft: false
author: "Jailani Rahman"
image: /images/blogs/week11.png
description: ""
toc:
---

<div class="h1"><u>PB Academic Week 10</u></div>

## 1. First Lesson

**Lesson Date:** 27/03/2023

### Lesson

The objective of this lesson plan was to equip students with the skills necessary to handle HTTP requests in their projects. The learning objective for this module was as follows:

Able to handle HTTP requests.
The activities included in this lesson plan were as follows:

During the lecture session, I conducted a brief assignment briefing, providing students with an overview of the task at hand.

In the practical session, I demonstrated how to send data with HTTP requests and highlighted the differences between the GET and POST methods. I also showcased how controllers handle HTTP requests, emphasizing the necessary steps involved.

During the exercise session, I facilitated the implementation of adding students, allowing students to practice and apply their knowledge of handling HTTP requests.

### Reflective Evaluation
During the exercise session, I unfortunately ran out of time and was unable to discuss the solution to the exercise with the students. To ensure they had access to the solution, I decided to share it through GitHub Gist. The solution can be found at the following link: https://gist.github.com/jailanihar/c714e5235c8d7a48a3e2eb6eb72a9931.

Additionally, I realized that the List<Student> ALL_STUDENTS = Arrays.asList(...) approach had a limitation. Due to the abstract nature of the List interface, it was not possible to add new data to it. To overcome this limitation, I advised the students to convert the List to an ArrayList and use the appropriate constructor to add the hardcoded students.

In future sessions, I will allocate more time for exercise discussions and ensure that students have the opportunity to review and understand the provided solutions. Furthermore, I will strive to anticipate any potential limitations or challenges associated with the code examples and provide appropriate guidance to the students in overcoming them.

Moving forward, I will continue to create an engaging learning environment and provide resources that support students' understanding of handling HTTP requests. I will also encourage students to seek clarification and assistance whenever they encounter difficulties, ensuring that their learning experience remains productive and effective.

  
## 2. Second Lesson

**Lesson Date:** 28/03/2023
  
### Lesson

The objective of this lesson plan was to ensure students understand and can apply Structured Query Language (SQL) in their database-related projects. The learning objective for this module was as follows:

Understand and apply Structured Query Language (SQL).
The activities included in this lesson plan were as follows:

During the lecture session, I showed the first part of a video https://www.youtube.com/watch?v=7S_tz1z_5bA to provide students with an introduction to databases and their wide application in various systems.

In the practical session, I focused on familiarizing students with MySQL using phpMyAdmin. I demonstrated how to create, choose, and delete databases in MySQL. Additionally, I showed students how to create, delete, and alter database tables. Practical examples were given to illustrate inserting and retrieving data from database tables, including retrieving data with conditions and using logical operators. I also demonstrated how to retrieve data from multiple database tables and edit existing data.

### Reflective Evaluation
During the practical session, I encountered an issue when covering updating and deleting data using SQL statements. Initially, I had planned to rely on the phpMyAdmin user interface for these operations. However, due to the absence of a primary key in the tables created during the practical, phpMyAdmin restricted access to these operations through its user interface. To address this limitation, I will ensure that next week, after creating tables with primary keys, I show the students how to perform these operations using both SQL statements and the phpMyAdmin interface.

Moving forward, I will allocate ample time to cover the necessary SQL operations, including updating and deleting data, to ensure students have a comprehensive understanding of these important concepts. I will also emphasize the significance of primary keys and demonstrate their implementation in practical examples. By doing so, I aim to provide students with a solid foundation in SQL and empower them to apply this knowledge effectively in their future database projects.

Furthermore, I will continue to explore additional resources and teaching materials to enhance students' understanding of SQL concepts and their practical applications. Encouraging active participation, addressing student queries, and providing hands-on exercises will remain key strategies in creating an engaging and effective learning experience.

---

## 3. Lesson Plan
{{<embed-pdf url="../resources/NEP_LP_S2_23_WK10_MJA.pdf">}}