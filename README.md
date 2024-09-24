# Educational-Initiatives

## Overview

This repository contains two exercises that demonstrate the usage of **Design Patterns** in Java, using various behavioral, creational, and structural patterns. Each pattern is illustrated with concrete examples as per the task requirements.

The tasks are divided into two exercises:
1. **Exercise 1:** Showcasing different behavioral, creational, and structural design patterns.
2. **Exercise 2:** Implementing a virtual classroom system using the **Command** pattern, with additional design patterns applied.



## Exercise 1: Design Pattern Demonstrations

Demonstrated the following design patterns:

### 1. Behavioral Design Patterns
- **Command Pattern:**
  - The command pattern is used to encapsulate a request as an object, thereby allowing for parameterization of clients with queues, requests, and operations. This pattern decouples the object that invokes the operation from the one that knows how to perform it.

- **Observer Pattern:**
  - The observer pattern allows one or more objects (observers) to get notified automatically when there is any change in the subject.

### 2. Creational Design Patterns
- **Abstract Factory Pattern:**
  - The abstract factory pattern provides an interface for creating families of related or dependent objects without specifying their concrete classes.

- **Builder Pattern:**
  - The builder pattern separates the construction of a complex object from its representation. This allows for step-by-step construction.

### 3. Structural Design Patterns
- **Composite Pattern:**
  - The composite pattern allows individual objects and compositions of objects to be treated uniformly.

- **Decorator Pattern:**
  - The decorator pattern allows behavior to be added to individual objects dynamically without affecting the behavior of other objects from the same class.

---

## Exercise 2: Virtual Classroom System

### Overview

The second exercise implements a **Virtual Classroom System** using the **Command Pattern**. This system manages classrooms, students, and assignments through commands that are executed dynamically based on user input.

### Design Pattern Used

1. **Command Pattern:**
   - Commands encapsulate requests to add a classroom, add a student, schedule an assignment, and submit an assignment. Each command can be executed separately, allowing the system to be easily extendable and flexible.

### Classes and Patterns in Use

- **ClassroomFacade:**
  - Acts as a facade to the system, providing a simplified interface to add classrooms, students, and assignments.

- **Command Classes:**
  - `AddClassroomCommand`
  - `AddStudentCommand`
  - `ScheduleAssignmentCommand`
  - `SubmitAssignmentCommand`

These command classes encapsulate various actions that can be executed by the system.

---

## How to Run the Application

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/virtual-classroom.git
   cd virtual-classroom
   ```

2. Compile the code:
   ```bash
   javac VirtualClassroomApp.java
   ```

3. Run the application:
   ```bash
   java VirtualClassroomApp
   ```

4. Sample commands:
   - `add_classroom Math101`
   - `add_student S123 Math101`
   - `schedule_assignment Math101 "Algebra Homework"`
   - `submit_assignment S123 Math101 "Algebra Homework"`

---

## Design Patterns Summary

| **Pattern**   | **Type**       | **Description**                                                                                                                                                   |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Command       | Behavioral      | Encapsulates a request as an object, allowing clients to parameterize objects with operations. Used to handle user inputs dynamically.                             |
| Observer      | Behavioral      | Notifies observers automatically when a subject changes. Used for notifying the classroom of assignment submissions.                                                |
| Abstract Factory | Creational      | Provides an interface for creating families of related objects. Used for creating classrooms, students, and assignments.                                           |
| Builder       | Creational      | Separates the construction of a complex object from its representation. Used for creating a `Classroom` object step by step.                                       |
| Composite     | Structural      | Treats individual objects and compositions uniformly. Used to represent a classroom containing students and assignments.                                           |
| Decorator     | Structural      | Dynamically adds behavior to objects without altering the original class. Can be used to add additional functionality to the `Assignment` class like grading. |

