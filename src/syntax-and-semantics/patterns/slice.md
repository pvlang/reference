# Slice Patterns

## Syntax

```
<slice-pattern-atom> ::= <identifier> (":" <type>)?
                       | "_" (":" <type>)?
                       | "is" <expression>
                       | "is" "in" <expression>
                       | "#" <pattern>

<slice-pattern> ::= "[" (<slice-pattern-atom> ",")* <slice-pattern-atom>? "]"
                  | "[" (<slice-pattern-atom> ",")* ".." (":" <type>)? ("as" <identifier>)? ("," <slice-pattern-atom> )* ","? "]"
```

## Semantics

Coming soon...
