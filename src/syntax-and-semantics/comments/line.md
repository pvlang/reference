# Line Comments

## Syntax

```
<line-comment> ::= "//" <utf8-code-point>* "\n"
                 | "//" <utf8-code-point>* <EOF>
```

## Semantics

- UTF-8 code points between `//` and `\n | EOF` are ignored by the compiler.
