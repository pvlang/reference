# Propositions

## Syntax

```
<proposition>  ::= <expression>
<propositions> ::= "{" (<proposition> ",")* <proposition>? "}"
```

## Semantics

- They must evaluate to a value of type **bool**.
- They must be able to be evaluated during compilation (e.g., sould not perform IO).
