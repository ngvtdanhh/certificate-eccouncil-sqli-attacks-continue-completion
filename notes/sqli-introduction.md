# Introduction to SQL Injection

SQL Injection (SQLi) is a code injection technique used to attack data-driven applications by inserting malicious SQL statements into input fields.  
It remains one of the most common web application vulnerabilities.

## Key Concepts
- Exploits improper input validation
- Allows attackers to read, modify or delete data
- Can lead to full DB compromise or authentication bypass

## Basic Payload Example
```sql
' OR '1'='1' --
```

## Prevention Overview

- Use parameterized queries (Prepared Statements)

- Implement proper input validation and escaping

- Limit DB privileges
