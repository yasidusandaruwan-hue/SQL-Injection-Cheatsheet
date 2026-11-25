# 🛡️ SQL Injection (SQLi) Cheatsheet

A practical reference guide covering how SQL Injection occurs, common attack patterns, and secure coding remediation in controlled lab environments.

---

## 🚀 Overview
SQL Injection happens when untrusted user input is directly concatenated into a database query without proper sanitization or parameterization, allowing an attacker to alter the intended SQL command structure.

---

## 📌 Core SQLi Concepts & Defenses

| Concept / Technique | How It Works | Risk / Impact | Prevention / Mitigation |
| :--- | :--- | :--- | :--- |
| **Authentication Bypass** | Manipulating login query conditions so they always evaluate to true. | Unauthorized access to user or admin accounts. | Use parameterized queries and strong authentication checks. |
| **UNION-Based SQLi** | Appending results of an injected query to the original query output. | Extracting data from other tables or databases. | Prepared statements, strict type casting, and least privilege. |
| **Error-Based / Boolean Logic** | Observing database errors or true/false response changes. | Inferring schema structure or hidden data. | Disable verbose DB errors in production; use parameterized queries. |
| **Parameterized Queries** | Binding user input as parameters rather than executable SQL syntax. | Prevents input from altering query structure. | Standard defense across modern web frameworks. |

---

## 🛠️ Defensive Best Practices
1. **Use Prepared Statements (Parameterized Queries):** Keep SQL query structure and user data strictly separate.
2. **Enforce Least Privilege:** Restrict database accounts to only the permissions required by the application.
3. **Validate & Cast Inputs:** Apply strict server-side validation and expected data types (e.g., integers for IDs).
4. **Hide Detailed Error Messages:** Avoid exposing raw database error details to end users.

---
*Created by Yasidu Sandaruwan | Cybersecurity Enthusiast*
