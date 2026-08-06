# 2. Relational Operator Overloading

Relational  operators have a special case that, they always comes in pair.

> ==Vanna khojeko k vanda,  relational operators aauta lai matra overload garere mildaina, aauta lai garo vane usko pair lai ni garnai parxa nava error aauxa==

**Operators:** `>`, `<`, `>=`, `<=`, `==`, `!=`

Return type is always **bool**.


#### Pairs of the operators

1.  >     < 
2. ==    !=
3. >=    <=

So hamle kunai aauta lets say,  >  lai garem overload vane qsn le na vane pani < lai pani garnai paro.  **Thats the rule**


ani hamle yesma ( ) && ( )  deedai chaining garxam,  j j fields xa sabko chain banaudai

### Syntax:

```csharp
public static bool operator <symbol>(ClassName a, ClassName b)
{
    return 
        (a.field1 <symbol> b.field1) &&
        (a.field2 <symbol> b.field2);
}
```

## Example

```cs
public static bool operator >(Graph a, Graph b)
{
    return 
        (a.x > b.x) &&
        (a.y > b.y);
}
```

> Remember the rule, jaile pair ma,  so aaba aauta lai gare paxi aarko ni paro, in this case  **>** ko pair vaneko  **<** ko ni garnai paro.


```cs
public static bool operator >(Graph a, Graph b)
{
    return 
        (a.x > b.x) &&
        (a.y > b.y);
}
```

For equality:

```csharp
public static bool operator ==(Graph a, Graph b)
{
    return 
        (a.x == b.x) &&
        (a.y == b.y);
}
```

For not equal:

```csharp
public static bool operator !=(Graph a, Graph b)
{
    return 
        (a.x != b.x) ||
        (a.y != b.y);
}
```

#### Note

Here is a catch, hamle k vaneko theyo vane hamle sabma  `&&` ko chain garne vaneko them, but 
-  Not equal  ( != ) ko case ma chai  `||` ko chain banauna parxa 
-  aaru sab ma && just  != ma chai ||

