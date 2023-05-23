---
title: "Week 13"
date: 2023-04-15
draft: false
author: "Jailani Rahman"
image: /images/blogs/week13.png
description: ""
toc:
---

## First Session

Lesson Date: 10/04/2023

The objective of this lesson plan was to enable students to apply the Java Persistence API (JPA) effectively in their database-related projects. The learning objective for this module was as follows:

Apply Java Persistence API (JPA) for data persistence.
The activities included in this lesson plan consisted of a practical session and an exercise, with a total duration of 2 hours.

During the practical session, which lasted for 1 hour 45 minutes, I demonstrated various aspects of implementing JPA in a Spring application. I started by showing students how to create Plain Old Java Objects (POJOs) to structure data in the database. I explained the purpose of annotations such as @Entity, @Table, @Id, @GeneratedValue, and @Column, and showcased their functionalities. It was emphasized that implementing a no-arg constructor in the POJO is mandatory. Additionally, I explained how to establish table relationships between two POJOs.

Following the practical session, a 15-minute exercise was given to the students, requiring them to complete the implementation of a Student class based on specific requirements. The requirements included setting the "id" field as the primary key and ensuring that the "name" field cannot be null.

During the final 30 minutes of the class, I facilitated students' laptops to ensure that their Spring Tools Suite was successfully connected to the database, providing them with a functional environment to work on their JPA implementations.

Reflective Evaluation:
Some students encountered errors during the practical session due to various reasons. These included creating the model class in a different package from the actual application implementation, forgetting to include the necessary @Entity and @Table annotations, connectivity issues to the internet even though it was emphasized that the MySQL server database.jailanirahman.com is hosted in Singapore, failure to install Spring JPA and the MySQL connector due to absence from previous sessions, and common basic Java mistakes.

The most concerning issues were reasons #3 and #5, as they indicate a lack of a solid grasp on the basics that were covered in earlier semesters. To address this, additional support and reinforcement of foundational Java concepts will be provided to ensure students have a strong foundation moving forward. Furthermore, it will be emphasized that connectivity to the internet is crucial for accessing necessary resources and dependencies.

To mitigate such issues in the future, it may be beneficial to conduct a brief review of important Java concepts and provide a troubleshooting guide or checklist to help students identify and address common mistakes.

---

## Second Session

Lesson Date: 11/04/2023

The objective of this lesson plan was to enable students to apply the Java Persistence API (JPA) effectively in their database-related projects. The learning objective for this module was as follows:

Apply Java Persistence API (JPA) for data persistence.
The activities included in this lesson plan consisted of a practical session and an exercise, with a total duration of 2 hours.

During the practical session, which lasted for 1 hour 30 minutes, I demonstrated various aspects of implementing JPA in a Spring application. I continued from the previous session by showing students the implementation of the Student class. I explained how to use the Data Access Object (DAO) interface to handle the persistence operations for the POJOs. I demonstrated the usage of DAO in the controller, retrieving all entities and a single entity using the DAO methods. Additionally, I showcased the implementation of custom methods in the DAO interface for specific data retrieval needs. Furthermore, I explained and demonstrated how to add, remove, and update data in the database using JPA.

Following the practical session, a 30-minute exercise was given to the students, requiring them to complete the CRUD (Create, Read, Update, Delete) implementation for the Group class.

Reflective Evaluation:
During the session, I realized that there was an issue with the code from the previous exercise that could potentially cause problems in this session. I spent 30 minutes rectifying the code to prevent any issues from arising. As a result, I was unable to cover the topics of deleting and updating data in this session. I will ensure to cover these topics in the next session to ensure students have a comprehensive understanding of all CRUD operations in JPA.

To improve the flow and efficiency of future sessions, it is important to thoroughly review and test the exercises in advance to identify any potential issues or conflicts with the subsequent sessions. Additionally, providing clear instructions and code templates for the exercises can help streamline the implementation process and allow more time for covering additional topics.

Overall, the session was productive, and students were able to grasp the concepts of JPA implementation. By addressing the pending topics in the next session, students will have a complete understanding of how to perform all CRUD operations using JPA.
