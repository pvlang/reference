# `string` Type

## Syntax

```
<string-type> ::= "string"
```

## Semantics

- It is basically a struct with **pointer: \*u8** and **length: usize**.
- It always points to a UTF-8 encoded buffer.
- It is just a view (i.e., it does not own the data that it points).
