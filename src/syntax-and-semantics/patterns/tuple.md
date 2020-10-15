# Tuple Patterns

## Syntax

```
<tuple-pattern-atom> ::= <identifier> (":" <type>)?
                       | "_" (":" <type>)?
                       | "is" <expression>
                       | "is" "in" <expression>
                       | "#" <pattern>

<tuple-pattern> ::= "(" (<tuple-pattern-atom> ",")* <tuple-pattern-atom>? ")"
                  | "(" (<tuple-pattern-atom> ",")* ".." (":" <type>)? ("as" <identifier>)? ("," <tuple-pattern-atom> )* ","? ")"
```

## Semantics

Coming soon...
