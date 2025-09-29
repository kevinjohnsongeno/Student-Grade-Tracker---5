# StudentLogin Database

**StudentLogin** is a simple system designed to manage and relate:

- Student records
- Student login credentials

This README outlines how to create the database schema and explains the purpose of each SQL operation used for joining and querying the two tables.

---

# Joining Students and StudentLogin Tables

This section explains the SQL commands used to join the `students` and `studentlogin` tables with different types of JOINs, demonstrating how to combine and analyze data from both tables.

---

## Commands Overview

### 1. Table Creation: `students`

- **Purpose:** Defines the student information storage with fields for `student_id` (auto-increment primary key), `student_name`, `batch`, and a unique `username`.  
- **Used for:** Storing core student details.

---

### 2. Table Creation: `studentlogin`

- **Purpose:** Defines the login credentials linked to students using foreign keys on `student_id` and `username`.  
- **Used for:** Managing login usernames and passwords that correspond to students.

---

### 3. INNER JOIN Query

- **Purpose:** Lists students who have successfully logged in by returning records where matching `student_id` exists in both tables.  
- **Used for:** Identifying students with active login credentials.

---

### 4. LEFT JOIN Query

- **Purpose:** Lists all students along with their login information, including students who do **not** have login data (shows `NULL` in login columns).  
- **Used for:** Finding students who have yet to create login credentials.

---

### 5. RIGHT JOIN Query

- **Purpose:** Lists all login records and their matching student information, including login entries without corresponding student records.  
- **Used for:** Identifying login records that may be orphaned or unlinked.

---

### 6. FULL OUTER JOIN Simulation (LEFT JOIN + RIGHT JOIN UNION)

- **Purpose:** Combines results of LEFT and RIGHT JOIN queries to produce a comprehensive view of all students and all login entries, whether matched or unmatched.  
- **Used for:** Merging data fully from both tables to detect all matches and discrepancies.

---

By understanding and using these SQL commands, it is efficient to manage and analyze student information along with the login credentials, ensuring data integrity and completeness.

---

