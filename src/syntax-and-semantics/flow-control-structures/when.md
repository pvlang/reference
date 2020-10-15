# When

## Syntax

```
<match> ::= <expression>
          | "in" <expression>
          | "some" <identifier>
          | "#" <pattern>
          | "_"

<arm> ::= (<match> "or")* <match> ("provided" <expression>)? "=>" <expression>

<when> ::= "when" <expression> "is" "{" (<arm> ",")* <arm>? "}"
```

## Semantics

Coming soon...
