# Turtleback-Zoo-Management-System


This repository contains the source code, SQL command files, and application programs for Phase 3 of the Turtleback Zoo Application Project. This phase focuses on the complete development of the database schema and a menu-driven application that supports asset management, daily zoo activity, and management reporting. The deliverable also documents any revisions made to the Phase 2 specifications along with the problems encountered and the solutions implemented.

---

## Project Overview

The Turtleback Zoo Management System is designed to streamline zoo operations through three core applications:

1. **Asset Management**  
   Provides utilities to insert, update, and view details for:
   - Animals
   - Buildings
   - Attractions
   - Employees (including hourly wages)
   - Other related entities

2. **Daily Zoo Activity**  
   Enables entry and review of daily activities such as:
   - Attraction attendance and revenue per showing
   - Concession daily revenue
   - Overall attendance numbers and revenue per attendee type

3. **Management and Reporting**  
   Offers management tools to generate critical reports for decision making, including:
   - Daily revenue reports by source with detailed line items and subtotals
   - Animal population reports by species (including status totals, monthly food cost, and staff cost estimates)
   - Reports on the top attractions (by total revenue) for a given period
   - Identification of the best revenue days in a month
   - Calculation of average revenue for attractions, concessions, and overall attendance over a specified period

---

## Database Schema and Implementation

### Database Creation
The database schema is designed with careful consideration of table relationships, primary keys, foreign keys, and data integrity. The schema includes (but is not limited to) the following tables:
- **Employee** – Stores employee details with self-referencing foreign keys for supervisors and a foreign key linking to HourlyRate.
- **HourlyRate** – Contains hourly wage information for employees.
- **Species, Animal, Building** – Manage information related to animal species, individual animals (with status and food cost), and zoo buildings.
- **RevenueTypes, ZooAdmission, Concession, AnimalShow, RevenueEvents** – Support financial data, tracking revenue sources from admissions, concessions, and attractions.
- **Enclosure** – Represents physical spaces assigned to animal exhibits.
- **Associative Tables** (e.g., ParticipatesIn, VeterinarianAnimal, AnimalCareSpecialistAnimal) – Define relationships between entities.
- **Additional Tables** for specialized roles such as Veterinarian, Animal Care Specialist, Maintenance, Customer Service, and Ticket Seller.

The SQL commands used to create and populate these tables are provided in the `SQL codes.pdf` file.

### Sample Data
Each table has been populated with ample sample data to illustrate all required tasks. The sample data is deterministic and designed to fully exercise the functionality of the system while maintaining data integrity.

---

## Application Programs

The application suite is implemented as a simple, menu-driven system with web-based interfaces. Key features include:

1. **Asset Management Interfaces**  
   - Insert, update, and delete operations for animals, buildings, attractions, and employees.
   - HTML/PHP pages for each entity allow zoo staff to manage assets easily.
   - Example pages include:
     - New Animal/Building/Attraction entry forms
     - Update/Delete functionality for each table
   - Source code for these pages is provided in the `HTML Codes.pdf` file.

2. **Daily Zoo Activity**  
   - Interfaces to record and view attendance, revenue from attractions, concessions, and admissions.
   - Detailed forms for inputting daily revenue and attendance data.
   - The user guide (`USERS GUIDE.pdf`) details navigation through these pages.

3. **Management and Reporting**  
   - Reports that summarize revenue by source, animal populations by species, top attractions by revenue, best revenue days, and average revenue computations.
   - The reporting functions are accessible via simple HTML forms that query the database and display results in tabular format.
   - Additional functionality includes input validation and clear display of computed statistics.

All application programs have been developed to run correctly with the provided database schema and sample data.
---
![image](https://github.com/user-attachments/assets/4729b396-2d13-4a7a-8d52-cbeb58b56805)

## Documentation and User Guide

A detailed user guide (`USERS GUIDE.pdf`) is included, providing:
- An overview of the system's purpose and target audience.
- Step-by-step navigation instructions for each application module.
- Descriptions of key features and how to use the system effectively.

---

## Conclusion

The Turtleback Zoo Management System is a comprehensive solution for managing zoo operations, from asset management and daily activity tracking to detailed management reporting. This project demonstrates a complete end-to-end implementation—from database design and data population to application development and user interface design. All source code, SQL command files, and documentation are included in this repository.

For additional details, please refer to the project report and user guide files provided.
