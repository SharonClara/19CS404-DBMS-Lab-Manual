# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
![566034685-7c46cd28-4f8d-4d4a-9eaa-1cf5e5744068](https://github.com/user-attachments/assets/a65f7b98-79b3-4ed2-88c4-b175f400598e)


### Entities and Attributes
<img width="1247" height="326" alt="image" src="https://github.com/user-attachments/assets/a0fd765d-e443-469f-9a1a-c9ca902040c3" />


### Relationships and Constraints
<img width="1053" height="375" alt="image" src="https://github.com/user-attachments/assets/80b9c6a7-0a33-480d-a4f1-7001c1b0e4f9" />


### Assumptions
A member can join multiple programs.
Trainers can be assigned to multiple programs.
Personal training sessions always involve one trainer and one member.

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
<img width="736" height="503" alt="566034823-0f0a54e2-adab-4a2e-8eb8-6d0970ae498a" src="https://github.com/user-attachments/assets/1dbbeac8-550f-47d3-a4f1-b98eb69f514f" />


### Entities and Attributes

<img width="1192" height="381" alt="image" src="https://github.com/user-attachments/assets/bc76325d-5b8c-41ad-906b-34a0ac5d9c66" />

### Relationships and Constraints
<img width="1156" height="328" alt="image" src="https://github.com/user-attachments/assets/87793383-a208-4786-a207-2c5074de5b0b" />


### Assumptions
A member can borrow multiple books, but each loan entry is for one book at a time.
FineAmount is calculated separately and stored in the Loan entity.
A room can host many events but an event can take place in only one room.

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:

<img width="741" height="525" alt="566034976-7382994b-a0eb-454e-9339-eb5557b540fa" src="https://github.com/user-attachments/assets/6b795e6c-b001-40e9-a5f2-73daccb2e80d" />

### Entities and Attributes
<img width="1264" height="384" alt="image" src="https://github.com/user-attachments/assets/d5274af1-0bb7-4287-b88c-a920aa3103e2" />


### Relationships and Constraints
<img width="990" height="375" alt="image" src="https://github.com/user-attachments/assets/ec3e5d6b-cdf3-4212-ac38-48a57b2ed441" />


### Assumptions
A customer may or may not make a reservation before ordering.
Each order contains one dish per entry (multiple dishes = multiple order entries).
Billing is done per reservation, not per individual order.
A waiter can serve multiple orders but an order is handled by exactly one waiter.

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
