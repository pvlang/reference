# Tuple Expressions

## Syntax

```
<tuple-expression> ::= "(" ")"
                     | "(" (<expression> ",")+ <expression>? ")"
```

## Semantics

- Inner `<expression>`s could be of any type.
- Type of them is **(@typeof(E1), @typeof(E2), ..., @typeof(EN))**.
