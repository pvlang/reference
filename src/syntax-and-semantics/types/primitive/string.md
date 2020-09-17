# `string` Type

## Syntax

```
<string-type> ::= "string"
```

## Semantics

- It's just a view (i.e., it does not own the data that it points).
- It always points to a UTF-8 encoded buffer.
- It's basically a struct with **pointer: \*u8** and **length: usize**.
