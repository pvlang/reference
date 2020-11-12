# Requires

## Syntax

```
<requires> ::= "requires" <propositions>
```

## Semantics

- They tell the compiler to verify that before the function is called, every `<proposition>` in `<propositions>` is **true**.
