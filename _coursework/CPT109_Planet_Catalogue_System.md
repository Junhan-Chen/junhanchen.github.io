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
