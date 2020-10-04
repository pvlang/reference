# When

## Syntax

```
<arm> ::= <expression> "=>" <expression>
        | "in" <expression> "=>" <expression>
        | "some" <identifier> "=>" <expression>
        | "#" <pattern> "=>" <expression>
        | "_" "=>" <expression>

<when> ::= "when" <expression> "is" "{" (<arm> ",")* <arm>? "}"
```

## Semantics

Coming soon...
