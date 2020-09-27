# Generic Types

## Syntax

```
<generic-type> ::= <identifier> "[" ((<type> | <expression>) ",")* (<type> | <expression>)? "]"
```

## Semantics

- They're used to referring types defined by `<type-definition-statement>`s.
- On ambiguous inputs, their parameters are parsed as an `<expression>` and, if necessary, converted to a `<type>` in a later stage of compilation.
