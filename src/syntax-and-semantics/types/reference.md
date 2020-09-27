# Reference Types

## Syntax

```
<immutable-reference-type> ::= "&" <type>
<mutable-reference-type>   ::= "&" "mut" <type>

<reference-type> ::= <immutable-reference-type>
                   | <mutable-reference-type>
```

## Semantics

- They use pointers underneath.
- They cannot be extended.
