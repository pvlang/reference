# Array Expressions

## Syntax

```
<array-expression> ::= "[" (<expression> ",")* <expression>? "]"
```

## Semantics

- Inner `<expression>`s must have the same type.
- Type of them is **\[ @typeof(Es) ~ @countof(Es) ]**.
