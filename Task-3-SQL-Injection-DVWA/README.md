# SQL Injection Demonstration using DVWA (Low Security)

## Project Overview

This project demonstrates a basic **SQL Injection (SQLi)** attack using **Damn Vulnerable Web Application (DVWA)** configured with the **Low** security level. The purpose of this project is to understand how SQL Injection vulnerabilities occur in web applications and how attackers can manipulate SQL queries when user input is not properly validated.

> **Note:** This demonstration was performed in a controlled local lab environment using DVWA for educational purposes only.

---

## Objective

* Install and configure DVWA on a local server.
* Set the DVWA security level to **Low**.
* Demonstrate a basic SQL Injection vulnerability.
* Understand how improper input validation can expose sensitive database information.
* Learn common mitigation techniques to prevent SQL Injection attacks.

---

## Tools Used

* Kali Linux
* Apache2
* MariaDB
* PHP
* DVWA (Damn Vulnerable Web Application)
* Firefox Web Browser

---

## Environment Setup

* Operating System: Kali Linux (Virtual Machine)
* Web Server: Apache2
* Database: MariaDB
* PHP Version: PHP 8.x
* DVWA Security Level: Low

---

## SQL Injection Demonstration

The vulnerable application accepts a **User ID** as input.

### Normal Input

```
1
```

Output:

```
ID: 1
First Name: admin
Surname: admin
```

### SQL Injection Payload

```
1' OR '1'='1
```

This payload modifies the SQL query so that the condition always evaluates to **TRUE**, allowing the application to return all records from the database instead of a single user.

Example of the vulnerable SQL query:

```sql
SELECT first_name, last_name
FROM users
WHERE user_id = '$id';
```

After the injected input is processed, the query effectively becomes:

```sql
SELECT first_name, last_name
FROM users
WHERE user_id = '1' OR '1'='1';
```

As a result, multiple user records are displayed.

---

## Impact of SQL Injection

SQL Injection vulnerabilities can allow attackers to:

* Retrieve sensitive information from databases.
* Bypass authentication mechanisms.
* Modify or delete database records.
* Gain unauthorized access to applications.
* Potentially execute administrative actions on vulnerable systems.

---

## Mitigation Techniques

SQL Injection can be prevented by:

* Using parameterized (prepared) SQL statements.
* Validating and sanitizing user input.
* Applying the principle of least privilege for database accounts.
* Avoiding dynamic SQL queries built from user input.
* Performing regular security testing and code reviews.
* Implementing Web Application Firewalls (WAFs).

---

## Project Structure

```
Task-3-SQL-Injection-DVWA/
│
├── README.md
├── sql_injection_exploit.sh
└── screenshots/
    ├── login_page.png
    ├── security_low.png
    ├── sqli_page.png
    └── sqli_result.png
```

---

## Conclusion

This project demonstrated how SQL Injection vulnerabilities can occur when applications directly include user input in SQL queries without proper validation. The demonstration was performed using DVWA in a controlled environment for educational purposes. Understanding these vulnerabilities helps developers implement secure coding practices and build more resilient web applications.
