# `decimal` Type

## Syntax

```
<decimal-type> ::= "decimal" "[" <expression> "," <expression> ","? "]"
```

## Semantics

- Its representation and size is unspecified.
- It can contain decimal numbers with up to **E1** whole digits and exactly **E2** fractional digits (e.g., `decimal[3, 2]` can contain the decimals between **0.00** and **999.99**).
- Its constant arguments must be of type **u32** and must not be bigger than **32**.
