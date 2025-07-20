## 🧪 Scenario: Search box reveals DB query results directly

📥 Input:

```sql
' UNION SELECT username, password FROM users --
```

📤 Query Constructed:

```sql
SELECT name, description FROM products WHERE name = '' UNION SELECT username, password FROM users --';
```

## 🔍 Explanation: The UNION keyword allows combining attacker-defined data into the response.

🎯 Impact: Leaks usernames and password hashes.

## 🛡️ Mitigation:

- Remove SQL error feedback to users

- Validate number and type of returned columns

- Apply strict input controls

