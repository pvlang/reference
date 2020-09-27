# Pointer Types

## Syntax

```
<pointer-type> ::= <immutable-pointer-type>
                 | <mutable-pointer-type>

<immutable-pointer-type> ::= "*" <type>
<mutable-pointer-type>   ::= "*" "mut" <type>
```

## Semantics

- They have the same size as **usize**.
