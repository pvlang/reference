# Struct Expressions

## Syntax

```
<struct-expression-atom> ::= <identifier>
                           | <identifier> ":" <expression>

<struct-expression-base> ::= "{" (<struct-expression-atom> ",")* <spread-expression> "}"
                           | "{" (<struct-expression-atom> ",")* <struct-expression-atom>? "}"

<struct-expression> ::= "@" <struct-expression-base>
                      | <item-expression> <struct-expression-base>
```

## Semantics

Coming soon...
