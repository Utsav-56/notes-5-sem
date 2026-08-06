## One memory trick

- Sabma yestai nai hune ho syntax sabma same ho j type ko vaye ni
- But `!` aayo vane chai aalik different case hune garxa teeyo khyal garnu paro

| Type       | Return            | Parameters                   | Format         |
| ---------- | ----------------- | ---------------------------- | -------------- |
| Binary     | ClassName         | `(ClassName a, ClassName b)` | `a op b`       |
| Relational | `bool`            | `(ClassName a, ClassName b)` | compare fields |
| Unary      | ClassName or bool | `(ClassName a)`              | one object     |

---

The simplest rule:

```
Binary      → two objects → return new object
Relational  → two objects → return true/false
Unary       → one object  → return new object
```

