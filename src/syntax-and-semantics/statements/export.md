# Export Statement

## Syntax

```
<item-export> ::= <path> ("as" <identifier>)?
<glob-export> ::= <path> "::" "*"
<nested-export> ::= <path> "::" <exports>

<export> ::= <item-export>
           | <glob-export>
           | <nested-export>

<exports> ::= "{" (<export> ",")* <export>? "}"

<export-statement> ::= "export" (<export> | <exports>) ";"
```

## Semantics

Coming soon...
