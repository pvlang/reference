# Struct Patterns

## Syntax

```
<struct-pattern-atom> ::= <identifier> (":" <type>)? ("as" <identifier>)?
                        | <identifier> (":" <type>)? ("as" (<identifier> | "_"))? "is" <expression>
                        | <identifier> (":" <type>)? ("as" (<identifier> | "_"))? "is" "in" <expression>
                        | <identifier> (":" <type>)? ("as" (<identifier> | "_"))? "is" "#" <pattern>

<struct-pattern> ::= "{" (<struct-pattern-atom> ",")* <struct-pattern-atom>? "}"
                   | "{" (<struct-pattern-atom> ",")* ".." (":" <type>)? ("as" <identifier>)? ","? "}"
```

## Semantics

Coming soon...
