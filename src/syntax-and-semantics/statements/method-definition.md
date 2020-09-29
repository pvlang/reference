# Method Definition Statement

## Syntax

```
<self-parameter> ::= "self"
                   | "&" "self"
                   | "&" "mut" "self"

<method-parameters> ::= "(" <self-parameter> ("," <identifier> ":" <type>)* ","? ")"

<method-definition-statement> ::= "const"? "fn" <identifier> <generic-parameters> <method-parameters> "=" <expression> ";"
```

## Semantics

Coming soon...
