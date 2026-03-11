# 📒 AddressBookApp

A **Spring Boot REST API application** for managing contacts in an Address Book.

This project demonstrates a **progressive implementation of Address Book features through 25 use cases**, covering REST APIs, file operations, database integration, multithreading, and external REST service communication.

The project follows a **Git Feature Branch Workflow**, where each feature is developed in a separate branch and later merged into the `dev` branch.

---

# 🚀 Features Implemented

The application supports:

- Creating and managing contacts
- REST API development using Spring Boot
- File storage operations (File IO, CSV, JSON)
- Database integration with MySQL using JDBC
- Multithreading for batch operations
- External API communication using JSON Server

---

# 🛠 Tech Stack

- ☕ **Java 17**
- 🌱 **Spring Boot**
- 📦 **Maven**
- 🔗 **REST APIs**
- 🐬 **MySQL Database**
- 🔌 **JDBC**
- 📄 **CSV & JSON File Handling**
- 📡 **JSON Server**
- 🧵 **Java Multithreading**
- 🐙 **Git & GitHub**

---

# 📂 Project Structure

```
AddressBookApp
│
├── controller
│      AddressBookController.java
│
├── service
│      AddressBookService.java
│      JSONServerService.java
│
├── db
│      AddressBookDBService.java
│
├── model
│      Contact.java
│      AddressBook.java
│
├── io
│      AddressBookFileService.java
│      AddressBookCSVService.java
│      AddressBookJSONService.java
│
└── AddressBookAppApplication.java
```

---

# 📊 Use Case Implementation

| UC | Feature |
|----|--------|
| UC1 | Address Book Spring Boot Project Setup |
| UC2 | Add Contact |
| UC3 | Edit Contact |
| UC4 | Delete Contact |
| UC5 | Add Multiple Contacts |
| UC6 | Multiple Address Books |
| UC7 | Prevent Duplicate Contacts |
| UC8 | Search Person by City or State |
| UC9 | View Persons by City or State |
| UC10 | Count Contacts by City or State |
| UC11 | Sort Contacts by Name |
| UC12 | Sort Contacts by City, State, Zip |
| UC13 | Read / Write Address Book using File IO |
| UC14 | Read / Write Address Book using CSV |
| UC15 | Read / Write Address Book using JSON |
| UC16 | Retrieve Contacts from Database |
| UC17 | Update Contact and Sync with Database |
| UC18 | Retrieve Contacts by Date Range |
| UC19 | Count Contacts by City or State (Database) |
| UC20 | Add Contact to Database |
| UC21 | Add Multiple Contacts using Multithreading |
| UC22 | Retrieve Contacts from JSON Server |
| UC23 | Add Entries to JSON Server |
| UC24 | Update Entry in JSON Server |
| UC25 | Delete Entry from JSON Server |

---

# 🌐 REST API Endpoints

## Contact Management

```
GET /contacts
POST /contacts
PUT /contacts/{id}
DELETE /contacts/{id}
```

## Database APIs

```
GET /contacts/db
POST /contacts/db/add
PUT /contacts/db/update
GET /contacts/db/date-range
GET /contacts/db/count/city
GET /contacts/db/count/state
```

## JSON Server APIs

```
GET /contacts/jsonserver
POST /contacts/jsonserver/add-multiple
PUT /contacts/jsonserver/update/{id}
DELETE /contacts/jsonserver/delete/{id}
```

---

# 🐬 MySQL Database Setup

### Create Database

```sql
CREATE DATABASE addressbook_db;
```

### Create Table

```sql
CREATE TABLE contacts (
 id INT PRIMARY KEY AUTO_INCREMENT,
 first_name VARCHAR(50),
 last_name VARCHAR(50),
 address VARCHAR(100),
 city VARCHAR(50),
 state VARCHAR(50),
 zip VARCHAR(10),
 phone VARCHAR(15),
 email VARCHAR(100),
 date_added DATE
);
```

---

# 🌐 JSON Server Setup

### Install JSON Server

```bash
npm install -g json-server
```

### Create File

```
db.json
```

### Example

```json
{
  "contacts": []
}
```

### Start Server

```bash
json-server --watch db.json --port 3000
```

### Server URL

```
http://localhost:3000/contacts
```

---

# 🧪 Testing APIs

You can test APIs using:

- **CURL**
- **Postman**
- **Browser (for GET requests)**

### Example

```bash
curl http://localhost:8080/contacts
```

---

# 🌿 Git Branch Strategy

The project follows a **Feature Branch Workflow**.

### Main Branches

```
main
dev
```

### Feature Branches

```
feature/UC1-create-contact
feature/UC2-add-contact
...
feature/UC25-delete-entry-jsonserver
```

Each use case is developed in a **separate branch** and merged into `dev` after completion.

---

# 🎯 Learning Outcomes

This project demonstrates:

- REST API development with **Spring Boot**
- **Layered architecture** (Controller → Service → DB/File)
- **Database integration using JDBC**
- **File handling with CSV and JSON**
- **Multithreading in Java**
- **External API integration using RestTemplate**
- **Version control using Git Feature Branching**

---
