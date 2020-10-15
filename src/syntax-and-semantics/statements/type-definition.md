# Type Definition Statement

## Syntax

```
<tuple-definition>   ::= "(" (<type> ",")* <type>? ")"
<struct-definition>  ::= "{" (<identifier> ":" <type> ",")* (<identifier> ":" <type>)? "}"
<variant-definition> ::= "(" "|"? (<type> | <type-definition>) ("|" (<type> | <type-definition>))+ ")"

<type-definition> ::= "trivial"? "type" <identifier> <generic-parameters>? ("=" (<tuple-definition> | <struct-definition> | <variant-definition>))?

<type-definition-statement> ::= <type-definition> ";"
```

## Semantics

Coming soon...
