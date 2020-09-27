# Reference Types

## Syntax

```
<reference-type> ::= <immutable-reference-type>
                   | <mutable-reference-type>

<immutable-reference-type> ::= "&" <type>
<mutable-reference-type>   ::= "&" "mut" <type>
```

## Semantics

- They use pointers underneath.
