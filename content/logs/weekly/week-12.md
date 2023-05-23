---
title: "Week 12"
date: 2023-04-08
draft: false
author: "Jailani Rahman"
image: /images/blogs/week12.png
description: ""
toc:
---

## First Lesson

Lesson Date: 03/04/2023

The objective of this lesson plan was to ensure students can apply Structured Query Language (SQL) effectively in their database-related projects. The learning objective for this module was as follows:

Apply Structured Query Language (SQL).
The activities included in this lesson plan were conducted during a practical session that lasted for 2 hours. The focus was on practical implementations and concepts related to SQL.

During the practical session, I covered various topics to enhance students' understanding and application of SQL. I demonstrated how to implement primary keys in database tables and provided examples of deleting and changing primary keys. Furthermore, I explained the concept of an Entity Relationship Diagram (ERD) and how to implement it in MySQL. I also showed students how to implement foreign keys in database tables, including examples of deleting and changing foreign keys. The benefits of using foreign keys were emphasized to highlight their significance in maintaining data integrity. Additionally, I explained how to implement auto-increment functionality in MySQL. Throughout the session, I reiterated that there are more advanced techniques available in MySQL beyond the basics covered in the lecture notes.

Reflective Evaluation:
The practical session was completed 30 minutes earlier than scheduled. I utilized the extra time to inquire about the progress of their assignments. It was observed that most of the groups were still in the designing stage, as they had prioritized assessments from other modules. This provided an opportunity for me to discuss their assignment requirements, address any concerns, and provide guidance for their ongoing projects.

To ensure that students remain engaged and actively working on their SQL assignments, I will allocate more time in the upcoming sessions specifically dedicated to discussing their progress, addressing challenges, and providing further assistance as needed. This will allow me to support them effectively in applying their SQL knowledge to practical scenarios.

Moreover, I will explore additional resources and examples to showcase advanced SQL techniques and applications. By introducing more complex SQL concepts, I aim to challenge students and expand their understanding beyond the basic concepts covered in the module. Encouraging students to explore and experiment with SQL in their assignments will foster a deeper comprehension of the subject matter and enhance their overall learning experience.

---

## Second Lesson

Lesson Date: 04/04/2023

The objective of this lesson plan was to ensure students can apply Structured Query Language (SQL) and utilize Spring Data JPA effectively in their database-related projects. The learning objective for this module was as follows:

Apply Structured Query Language (SQL) and Spring Data JPA.
The activities included in this lesson plan consisted of a lecture session and a practical session, with a total duration of 2 hours.

During the lecture session, which lasted for 1 hour 30 minutes, I covered various topics related to Spring Data JPA and its integration with MySQL. I started by defining Spring Data JPA and explained how to configure it within a Spring application. Furthermore, I discussed the MySQL connector and demonstrated the configuration process for integrating it with a Spring application. I explained how to configure the Spring application to connect to a MySQL database by modifying the properties file. I also emphasized the importance of using POJOs to structure data in the database and introduced relevant annotations such as @Entity, @Table, @Id, @GeneratedValue, and @NotNull. Examples of POJOs that represent data in a database were provided to illustrate the concepts. It was emphasized that a no-arg constructor must be implemented in the POJO. Additionally, I defined Data Access Objects (DAOs) and explained how to implement the CrudRepository interface to handle POJOs. I covered the methods available in the DAO, such as delete, exists, findAll, findOne, and save. Furthermore, I explained how to utilize the DAO in the controller to interact with the database, including retrieving all entities, retrieving a single entity, implementing custom methods in the DAO, adding data to the database, removing data from the database, and updating data in the database.

During the practical session, which lasted for 30 minutes, I facilitated students in connecting their laptops to the database using Spring Tools Suite. The aim was to ensure that students had a functioning environment to work with Spring Data JPA and MySQL.

Reflective Evaluation:
As anticipated, there were several errors encountered by students when installing the dependencies for Spring JPA and the MySQL connector. The typical issues were related to the instability of the school's student internet, causing interruptions during the installation process and resulting in errors in their Spring projects. However, by the end of the class, all issues were resolved, and students were able to successfully connect their projects to the database.

Another important note is that the dependency "mysql.mysql-connector-java" is no longer available. It has been replaced with the following:

```
<groupId>com.mysql</groupId>
<artifactId>mysql-connector-j</artifactId>
```

To further support students in their understanding and implementation of Spring Data JPA and SQL, additional resources, examples, and practice exercises will be provided. Furthermore, troubleshooting common issues encountered during the setup process will be addressed proactively in future sessions to minimize disruptions and ensure smooth progress for all students.
