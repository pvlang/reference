# Type Definition Statement

## Syntax

```
<tuple-definition>   ::= "(" (<type> ",")* <type>? ")"
<struct-definition>  ::= "{" (<identifier> ":" <type> ",")* (<identifier> ":" <type>)? "}"
<variant-definition> ::= "(" "|"? <type> ("|" <type>)+ ")"

<type-definition> ::= <tuple-definition>
                    | <struct-definition>
                    | <variant-definition>

<type-definition-statement> ::= "trivial"? "type" <identifier> <generic-parameters>? ("=" <type-definition>)? ";"
```

## Semantics

Coming soon...
