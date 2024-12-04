# Entity-Relationship Model: Gym Management System

## Overview
This project designs an Entity-Relationship (ER) model for a gym management system based on the given requirements. The ER model helps to structure the data and relationships efficiently for database implementation.

## Requirements

1. **Gymnasium:**
   - A gym chain with multiple branches, each identified by its name, address, and telephone number.

2. **Member:**
   - Members register at a gym and provide personal details like name, address, date of birth, and gender.
   - Each member is associated with only one gym.

3. **Session:**
   - Sessions are characterized by their type of sport, schedule, and a maximum capacity of 20 members.
   - A session takes place in a gym and can have up to 20 members.

4. **Coach:**
   - Each session can be led by up to 2 coaches, who have details like name, age, and specialty.

## ER Model Components

### **Entities**
1. **Gymnasium**
   - Attributes: GymID (PK), Name, Address, Telephone Number.

2. **Member**
   - Attributes: MemberID (PK), Last Name, First Name, Address, Date of Birth, Gender.

3. **Session**
   - Attributes: SessionID (PK), Type of Sport, Schedule, Max Capacity (Default: 20).

4. **Coach**
   - Attributes: CoachID (PK), Last Name, First Name, Age, Specialty.

### **Relationships**
1. **Registers:**
   - Relationship between `Gymnasium` and `Member`.
   - Cardinality: 1 Gymnasium : *N* Members.

2. **Hosts:**
   - Relationship between `Gymnasium` and `Session`.
   - Cardinality: 1 Gymnasium : *N* Sessions.

3. **Attends:**
   - Relationship between `Session` and `Member`.
   - Cardinality: 1 Session : *N* Members (Max: 20).

4. **Leads:**
   - Relationship between `Session` and `Coach`.
   - Cardinality: 1 Session : 2 Coaches (Max).

5. **Participates:**
   - Relationship between `Coach` and `Session`.
   - Cardinality: 1 Coach : *N* Sessions.

## ER Diagram
[Include a screenshot or attach a PDF of the ER diagram.]

## Tools Used
- ER Diagram Tool: [Tool Name] (e.g., Lucidchart, Draw.io, Visio)

## Author
Created by [Your Name]. Feedback and contributions are welcome!
