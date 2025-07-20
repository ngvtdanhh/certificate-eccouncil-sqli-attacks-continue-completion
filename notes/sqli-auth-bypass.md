# SQL Injection for Authentication Bypass

## Scenario
Login forms are common targets for SQLi. If inputs are not sanitized, attackers can bypass auth controls.

## Classic Payloads
```sql
' OR 1=1 --
' OR 'a'='a
admin' -- 
```

## Real-World Impact

- Unauthorized access to admin panels

- Privilege escalation

- Session hijacking

## Mitigation

- Use ORM or parameterized queries

- Implement multi-factor authentication

- Monitor unusual login behavior
