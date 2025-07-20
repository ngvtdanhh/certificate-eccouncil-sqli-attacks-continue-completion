## 🧪 Scenario: Error messages are visible when input breaks SQL syntax

📥 Input:

```sql
' AND 1=CONVERT(int, (SELECT @@version)) --
```

📤 Behavior: Returns verbose SQL Server version if unhandled.

## 🔍 Explanation: Exploits error messages to extract DBMS information.

🎯 Impact: Reveals DBMS type and version (e.g., SQL Server 2017), guiding tailored payloads.

## 🛡️ Mitigation:

- Suppress SQL errors from reaching the front-end

- Use generic error messages

- Enable logging for failed input parsing



