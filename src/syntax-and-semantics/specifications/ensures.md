# Ensures

## Syntax

```
<ensures> ::= "ensures" <propositions>
```

## Semantics

- They tell the compiler to verify that after the function is called, every `<proposition>` in `<propositions>` is **true**.
