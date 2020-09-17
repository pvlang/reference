# Identifiers

## Syntax

```
<identifier> ::= [A-Za-z] "_"? ([A-Za-z0-9] "_"?)*
               | "_" ([A-Za-z0-9] "_"?)+
```
## Semantics

- `_` is not an identifier by itself.
- `_` in the beginning indicates the symbol may not be used and it's alright.
- `_` is not allowed consecutively to improve readability.
- `_` could be used in the end to form keyword-like identifiers (e.g. `for_`, `type_`, `extension_`).
