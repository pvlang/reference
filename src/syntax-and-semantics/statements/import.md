# Import Statement

## Syntax

```
<item-import> ::= <path> ("as" <identifier>)?
<glob-import> ::= <path> "::" "*"
<nested-import> ::= <path> "::" <imports>

<import> ::= <item-import>
           | <glob-import>
           | <nested-import>

<imports> ::= "{" (<import> ",")* <import>? "}"

<import-statement> ::= "import" (<import> | <imports>) ";"
```

## Semantics

Coming soon...
