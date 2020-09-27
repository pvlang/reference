# Slice Types

## Syntax

```
<slice-type> ::= <immutable-slice-type>
               | <mutable-slice-type>

<immutable-slice-type> ::= "[" <type> "]"
<mutable-slice-type>   ::= "[" "mut" <type> "]"
```

## Semantics

- They're basically a struct with **pointer: \*T** (or **\*mut T**) and **length: usize**.
