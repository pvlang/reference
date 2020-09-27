# Slice Types

## Syntax

```
<immutable-slice-type> ::= "[" <type> "]"
<mutable-slice-type>   ::= "[" "mut" <type> "]"

<slice-type> ::= <immutable-slice-type>
               | <mutable-slice-type>
```

## Semantics

- They're basically a struct with **pointer: \*T** (or **\*mut T**) and **length: usize**.
- They are owned by the **core** project.
