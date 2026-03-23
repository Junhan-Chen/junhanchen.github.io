---
title: "Planet Catalogue System"
permalink: /coursework/CPT109_Planet_Catalogue_System/
author_profile: true
---

**Team:** Junhan Chen, Shengda Gao, Yiwen Wang, Yang Tian, Siyuan Lin  
**Course:** CPT109 C Programming and Software Engineering 1  
**Institution:** Xi'an Jiaotong-Liverpool University  
**Date:** Nov 2024 – Dec 2024  
**Language:** C (C90)

---

# Project Overview

This project involves the development of a **Planet Catalogue System**, a C-based software application designed to manage, search, and analyse planetary data for research purposes.

The system was implemented as a modular program, supporting multiple user roles (Admin and Researcher) and providing functionalities such as planet data management, account handling, search and retrieval, and statistical reporting.

---

# Problem Specification

## Overall Requirement

The system was developed as a C-based software application for managing and analysing planetary data.

It provides a structured environment for storing, retrieving, and processing information related to planets and user activities.

The main functionalities of the system include:

- **Planet Management**: storing and maintaining attributes such as name, type, size, and distance from the star  
- **User Accounts**: managing researcher accounts with unique identifiers  
- **Search and Retrieval**: querying planets based on different attributes  
- **Statistical Reporting**: generating statistics on catalogued, discovered, and observed planets  

The system supports two user roles:

- **Admin**
- **Researcher**

Each role is associated with different functionalities and access permissions.

---

## Admin Functional Requirements

The admin user is responsible for managing both planetary data and system users.

### Planet Data Management

- Add new planet records  
- Modify existing planet attributes  
- Delete planet records  

### Statistics Access

- View total number of catalogued planets  
- View number of discovered planets  
- View number of observed planets  

### Researcher Account Management

- Create researcher accounts  
- Modify account information  
- Delete researcher accounts  
- Monitor researcher activity  

---

## Researcher Functional Requirements

The researcher user focuses on interacting with planetary data.

### Planet Search and Retrieval

- Search planets by name, type, or other attributes  
- View detailed information of selected planets  

### Account Management

- Register a new account  
- Modify personal account information  
- View previous activity records

---

# Analysis

## Data Structure Design

The system is designed based on structured data representations for both planetary data and user accounts.

Two main data types are defined:

- **Planet structure**
- **User (Researcher/Admin) structure**

The planet structure stores key attributes such as:

- name  
- type  
- size  
- distance from the star  

The user structure stores:

- account ID  
- username  
- role (Admin or Researcher)  
- activity-related information  

To manage multiple records efficiently, the system uses **linked data structures**, allowing dynamic insertion and deletion of data without fixed size limitations.

---

## System Architecture

The system follows a modular design, where different functionalities are organised into independent modules.

The overall workflow of the system can be summarised as:

1. User login or registration  
2. Role identification (Admin or Researcher)  
3. Access to role-specific menu  
4. Execution of selected functions  
5. Return to menu or exit  

This structure ensures that the program remains organised and scalable, with clear separation between different functionalities.

---

## Functional Modules

The system is divided into several functional modules:

### Authentication Module

- User login  
- User registration  
- Role verification  

### Planet Management Module (Admin)

- Add planet  
- Modify planet  
- Delete planet  

### Search Module

- Search by name  
- Search by type  
- Display detailed planet information  

### Statistics Module

- Count catalogued planets  
- Count discovered planets  
- Count observed planets  

### Account Management Module

- Create accounts  
- Modify account information  
- Delete accounts  
- Track user activity  

Each module is designed to operate independently while interacting with shared data structures.

---

## Program Flow

The program is implemented as a menu-driven system.

After login, users are directed to different menus based on their roles:

- **Admin Menu**
- **Researcher Menu**

Each menu provides access to relevant functionalities, and users can repeatedly perform operations until they choose to exit the system.

This approach ensures usability and allows clear interaction between the user and the system.

## System Architecture

The system follows a modular design, where different functionalities are organised into independent modules.

<figure style="text-align:center;">
  <img src="/images/CPT109_SystemFlow.png" width="600">
  <figcaption><em>Figure 1. System workflow from login to function execution.</em></figcaption>
</figure>
<br>

The overall workflow of the system can be summarised as:

1. User login or registration  
2. Role identification (Admin or Researcher)  
3. Access to role-specific menu  
4. Execution of selected functions  
5. Return to menu or exit  

---

# Implementation

## Overview

The system was implemented in C using a modular structure.  
Each functionality was encapsulated into separate functions, allowing clear organisation of the program and easier maintenance.

The implementation integrates:

- structured data types  
- linked data structures  
- file-based storage  
- menu-driven interaction  

---

## Data Storage and File Handling

Planet data and user account information are stored using external files.

- Planet data is stored in a file (e.g. `planetcat.txt`)  
- User account data is stored separately  

File operations are implemented using standard C functions:

- `fopen()` for opening files  
- `fprintf()` for writing data  
- `fread()` / `fgets()` for reading data  
- `fclose()` for closing files  

This approach allows persistent storage of data across program executions.

---

## Dynamic Data Management

The system uses **dynamic memory allocation** and **linked lists** to manage data.

- `malloc()` is used to allocate memory for new records  
- Linked lists are used to store and traverse planet and user data  

This design enables:

- flexible insertion and deletion of records  
- efficient traversal for search operations  
- avoidance of fixed-size data limitations  

---

## Core Functional Implementation

### Planet Data Management (Admin)

- `increasep1()` is used to add new planet data  
- `modifyPlanet()` updates existing records  
- `deletePlanet()` removes planet entries  

These functions operate by:

1. locating the target record in the linked list  
2. modifying or deleting the data  
3. updating the file to reflect the changes  

---

### Search Functionality (Researcher)

- `searchPlanet()` allows users to search for planets based on different attributes  

The implementation:

- takes user input  
- traverses the linked list  
- compares values using `strcmp()` or numerical checks  
- returns matching planet data  

---

### Account Management

- `creatacc()` is used to create new accounts  
- `modifyAccount()` updates user credentials  

The system ensures:

- unique account identification  
- validation of user input  
- persistent storage in file  

---

### Statistics Function

- `viewStatistics()` calculates and displays system statistics  

This includes:

- number of catalogued planets  
- number of discovered planets  
- number of observed planets  
- number of registered users  

---

## Program Interaction

The system is implemented as a **menu-driven interface**.

- `mainmenu()` displays the main system menu  
- Different menus are presented based on user role  

User interaction is handled using:

- `printf()` for displaying options  
- `scanf()` / `fgets()` for input  

This structure enables continuous operation until the user chooses to exit the program.
