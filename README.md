# SQL Server Stored Procedures (Database Programming Case Study)

![Database](https://img.shields.io/badge/database-SQL%20Server-blue)
![Language](https://img.shields.io/badge/language-SQL-yellow)
![Backend](https://img.shields.io/badge/backend-C%23-green)
![Architecture](https://img.shields.io/badge/Architecture-Database%20Layer-purple)
![Project Type](https://img.shields.io/badge/Project%20Type-Engineering%20Case%20Study-orange)

---

# Overview

This project demonstrates the implementation of **SQL Server Stored Procedures** for database-level business logic.

Stored procedures allow applications to execute precompiled SQL logic directly within the database, improving:

- performance
- security
- maintainability
- data consistency

The project illustrates how stored procedures can be used as part of a backend architecture integrated with **C# applications**.

---

# Case Study

## Problem

Applications often need to perform repeated database operations such as:

- inserting records
- validating data
- encapsulating business logic
- enforcing database rules

Embedding all SQL logic directly in application code can lead to duplication and poor maintainability.

---

## Solution

Stored procedures are used to centralize database operations inside the SQL Server engine.

This approach provides:

- reusable database logic
- improved query performance
- stronger security control
- simplified backend integration

---

# Example Stored Procedure

Example of a stored procedure used for inserting records:

```sql
CREATE PROCEDURE uspInserirTelefoneTipo
(
    @IDTelefoneTipo INT,
    @DescTelefoneTipo VARCHAR(30)
)
AS
BEGIN

INSERT INTO tblTelefoneTipo
(
    IDTelefoneTipo,
    DescTelefoneTipo
)

VALUES
(
    @IDTelefoneTipo,
    @DescTelefoneTipo
)

END
```

# SQL Server Implementation
Stored Procedure Creation
Database Structure
Stored Procedure Execution

# Architecture

The architecture demonstrates how stored procedures integrate with application layers.
```text

Application (C#)
       │
       ▼
Data Access Layer
       │
       ▼
SQL Server Stored Procedures
       │
       ▼
Database Tables
```
This structure helps separate application logic from database logic.

# Folder Structure
```text

StoredProcedure
│
├── AcessoBancoDados
├── Apresentacao
├── Negocios
├── ObjetoTransferencia
└── SQL Scripts
```
Layer explanation:
| Layer | Responsibility |
| :---: | :---: |
| Apresentação | Application interface |
| Negócios | Business logic |
| Acesso Banco de Dados | Database communication |
| Objeto Transferência | Data transfer objects |

# Technologies

Backend

SQL Server

Stored Procedures

C#

Database Tools

Microsoft SQL Server Management Studio (SSMS)

# How to Run
1 Clone repository
```text
git clone
```
2 Open SQL Server Management Studio
Connect to a SQL Server instance

3 Execute stored procedure scripts
Run the SQL scripts to create:
tables
stored procedures

4 Execute procedures
Example:
```text
EXEC uspInserirTelefoneTipo
```
# Learning Outcomes

This project demonstrates:

SQL Server stored procedure development

database layer architecture

backend integration with C#

database performance optimization techniques

encapsulation of database logic

# Author

Thiago Reis Lima

LinkedIn
```text
https://www.linkedin.com/in/thiago-lima-2a5896166
```
