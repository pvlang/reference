# Struct Types

## Syntax

```
<struct-type> ::= "{" (<identifier> ":" <type> ",")* (<identifier> ":" <type>)? "}"
```

## Semantics

- They're anonymous structs.
- They're structurally equivalant (i.e., **{ x: f64, y: f64 }**, and **{ y: f64, x: f64 }** are the same type).
