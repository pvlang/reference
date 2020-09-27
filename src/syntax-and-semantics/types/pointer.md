# Pointer Types

## Syntax

```
<immutable-pointer-type> ::= "*" <type>
<mutable-pointer-type>   ::= "*" "mut" <type>

<pointer-type> ::= <immutable-pointer-type>
                 | <mutable-pointer-type>
```

## Semantics

- They have the same size as **usize**.
- They are owned by the **core** project.
