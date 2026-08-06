
# 3. Unary Operator Overloading

**Operators:** `+`, `-`, `++`, `--`, `!`, `~`

Only **one object** is passed.

### Syntax:

```csharp
public static ClassName operator <symbol>(ClassName a)
{
    return new ClassName(
        <symbol>a.field1,
        <symbol>a.field2
    );
}
```

---

### Example: Unary Minus

```csharp
public static Graph operator -(Graph a)
{
    return new Graph(
        -a.x,
        -a.y
    );
}
```

---

### Example: Increment `++`

```csharp
public static Graph operator ++(Graph a)
{
    return new Graph(
        ++a.x,
        ++a.y 
    );
}
```

---

### Example: Logical NOT `!`

Here the return type changes because `!` normally gives a condition:

```csharp
public static bool operator !(Graph a)
{
    return a.x == 0 && a.y == 0;
}
```

---

> **Notice:** Yaha pani  `!` aauda return type ra syntax aalik change vayo,  so  `!` aauda chai aalik different hunxa vanera bujhna paro, 
> 


