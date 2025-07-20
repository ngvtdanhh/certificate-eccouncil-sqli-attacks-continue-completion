## 🧪 Scenario: Login form vulnerable to SQLi in the username field

📥 Input (username):

```sql
admin' OR '1'='1' --
```

📤 Interpreted Query:

```sql
SELECT * FROM users WHERE username = 'admin' OR '1'='1' -- ' AND password = '...';
```

## 🔍 Explanation: ' OR '1'='1' -- causes the WHERE clause to always return true, bypassing authentication.

🎯 Impact: Admin-level access without credentials.

## 🛡️ Mitigation:

- Use parameterized queries (e.g., cursor.execute("SELECT * FROM users WHERE username = ?", [username]))

- Enforce proper input sanitization
