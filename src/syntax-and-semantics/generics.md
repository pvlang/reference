# Generics

## Syntax

```
<generic-parameter> ::= <identifier> | <identifier> ":" <type>
<generic-parameters> ::= "[" <generic-parameter> ("," <generic-parameter>)* ","? "]"

<generic-argument>  ::= <type> | <expression>
<generic-arguments> ::= "[" <generic-argument> ("," <generic-argument>)* ","? "]"
```

## Semantics

- On ambiguous inputs, generic argument is parsed as an `<expression>` and, if necessary, converted to a `<type>` in a later stage of compilation.
