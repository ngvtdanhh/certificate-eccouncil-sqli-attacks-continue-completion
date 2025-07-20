# UNION-Based SQL Injection

## Concept
UNION-based injection leverages the SQL UNION operator to combine results from different queries, revealing hidden data.

## Requirements
- Number of columns must match
- Data types of SELECT statements must align

## Example
```sql
' UNION SELECT username, password FROM users --
```

- Testing Columns

```sql
' ORDER BY 3 --
' UNION SELECT NULL, NULL, NULL --
```

## Prevention

- Disable error-based output

- Sanitize and whitelist user inputs
