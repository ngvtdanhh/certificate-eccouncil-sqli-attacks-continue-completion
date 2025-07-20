## 🧪 Scenario: The app doesn’t display output but behaves differently on valid vs. invalid input

📥 Payload:

```sql
1' AND IF(1=1, SLEEP(5), 0) --
```

📤 Behavior: Response delayed by 5 seconds if true.

## 🔍 Explanation: Time delay is used to infer Boolean results without visible output.

🎯 Impact: Attackers enumerate data bit-by-bit via response timing.

## 🛡️ Mitigation:

- Enforce input validation (numeric-only if expected)

- Use web application firewalls to block such patterns

- Rate-limit suspicious requests
