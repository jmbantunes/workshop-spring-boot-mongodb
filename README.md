
# Object-Oriented Programming with Java - MongoDB Project

## Overview

This project provides a comprehensive introduction to integrating MongoDB with a Spring Boot application. You'll learn how to implement CRUD operations, use MongoDB’s document-oriented paradigm, and understand the differences between document-based and relational databases. Through practical exercises, you will explore data modeling, associations, and perform various queries using Spring Data and MongoRepository.

## Objectives
By the end of this project, you will be able to:
- Understand the differences between document-oriented and relational databases.
- Implement basic CRUD operations with Spring Boot and MongoDB.
- Create associations between objects in MongoDB (nested objects and references).
- Use Spring Data to perform queries on MongoDB.
- Reflect on design decisions when working with a NoSQL database like MongoDB.

## Prerequisites
To follow this project, you will need:
- Basic understanding of Java and Spring Boot.
- Familiarity with MongoDB, a NoSQL document-based database.
- A working development environment with Spring Boot and MongoDB installed.

## Installation Guide

### MongoDB Setup
Follow the appropriate instructions based on your operating system to install MongoDB. Ensure that MongoDB is running locally on your machine before continuing with the project.

For Windows, after downloading and installing MongoDB, ensure the MongoDB service is running, and you have set the necessary paths in your system’s environment variables. On macOS, you can install MongoDB using Homebrew and configure it to run in the terminal.

## Spring Boot Project Setup

### Creating the Project
1. Use your preferred IDE (e.g., IntelliJ IDEA, Eclipse, Spring Tool Suite) to create a new Spring Boot project.
2. Choose the necessary dependencies, ensuring you include "Spring Web" and "Spring Data MongoDB."
3. After setting up, run the application on your local machine to verify that Spring Boot is working correctly.

### Connecting to MongoDB
Configure your application to connect to MongoDB. Set the MongoDB URI in the `application.properties` file to point to your local MongoDB instance.

## Defining MongoDB Entities

### User Entity
Start by creating a `User` entity class. In this entity, you will define basic attributes such as `name` and `email`. You will also add the `@Document` annotation to tell Spring Boot that this class is a MongoDB document, and `@Id` to specify the primary key field.

### CRUD Operations
Implement basic CRUD (Create, Read, Update, Delete) operations for the `User` entity. Create endpoints for creating new users, fetching users, updating user details, and deleting users.

## Repository and Service Layer

### Repository Layer
Define a `UserRepository` interface that extends `MongoRepository`. This repository will handle basic CRUD operations provided by MongoDB.

### Service Layer
Implement a `UserService` class to manage business logic, such as creating users, updating data, and querying users from the database.

## Handling Associations in MongoDB

### Nested Objects vs References
Learn the differences between using embedded (nested) objects and references in MongoDB. Embedded objects are useful for storing related data directly within the document, while references create links between documents.

### Implementing Associations
In this project, you will implement both types of associations:
- **Nested Objects**: For attributes that are part of the document itself.
- **References**: For attributes that refer to other documents.

## Querying Data

### Simple Queries
You will implement simple queries, such as finding users or posts based on their attributes. Spring Data MongoDB makes it easy to create custom query methods in your repository interfaces.

### Complex Queries with `@Query`
Learn how to use the `@Query` annotation to execute more complex queries, such as finding documents with specific conditions across multiple fields.

### Queries with Multiple Criteria
You will implement queries that involve multiple criteria, such as filtering documents based on date ranges or specific keywords.

## DTO Pattern

### What is a DTO?
A Data Transfer Object (DTO) is a design pattern used to transfer data between different layers of an application, especially when data needs to be aggregated or filtered. In this project, you will create DTO classes to return specific data from your MongoDB documents without exposing sensitive or unnecessary information.

## Exception Handling and Error Management

### Custom Exceptions
You will learn how to handle errors by creating custom exceptions and using them to handle situations like object not found in the database.

### Global Error Handling
Implement a global error handler for the API, ensuring that any exceptions thrown are handled gracefully and provide useful error messages to the client.

## Advanced Features

### Pagination and Sorting
Spring Data MongoDB supports pagination and sorting. You will implement endpoints to handle pagination and sorting, making your API more flexible and efficient.

### Data Projection
You will learn how to project data from MongoDB documents into different formats, such as DTOs, for specific client-side needs.

## Conclusion
By completing this project, you will have a deeper understanding of MongoDB and how to integrate it with Spring Boot applications. You will be able to apply document-oriented data modeling, implement CRUD operations, handle associations, and write complex queries. This project serves as a foundational experience in working with MongoDB and Spring Boot.
