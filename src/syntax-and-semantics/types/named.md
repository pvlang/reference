# Named Types

## Syntax

```
<generic-parameter>  ::= <type> | <expression>
<generic-parameters> ::= <generic-parameter> ("," <generic-parameter>)* ","?

<named-type> ::= <path> ("[" <generic-parameters> "]")?
```

## Semantics

- Named types are used to referring types defined by either `<type-definition-statement>`s or `<machine-definition-statement>`s.
- On ambiguous inputs, their generic parameters are parsed as an `<expression>` and, if necessary, converted to a `<type>` in a later stage of compilation.
