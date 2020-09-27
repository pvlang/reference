# Block Comments

## Syntax

```
<block-comment> ::= "/*" <utf8-code-point>* "*/"
                  | "/*" <utf8-code-point>* <block-comment> <utf8-code-point>* "*/"
```

## Semantics

- UTF-8 code points between `/*` and the matching `*/` are ignored by the compiler.
- They can be nested (e.g., `/* foo /* bar */ baz */`).
