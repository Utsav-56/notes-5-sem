
# 1. Binary Operator Overloading

**Operators:** `+`, `-`, `*`, `/`, `%`, `&`, `|`, `^`, `<<`, `>>`

### Syntax:

```csharp
public static ClassName operator <symbol>(ClassName a, ClassName b)
{
    return new ClassName(
        a.field1 <symbol> b.field1,
        a.field2 <symbol> b.field2
    );
}
```


### Example:

```csharp
public static Graph operator +(Graph a, Graph b)
{
    return new Graph(
        a.x + b.x,
        a.y + b.y
    );
}
```

Here we assume that there is a class named graph with fields of x and y.


