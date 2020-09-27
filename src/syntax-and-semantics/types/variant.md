# Variant Types

## Syntax

```
<variant-type> ::= "(" "|"? <type> ("|" <type>)+ ")"
```

## Semantics

- They are tagged.
- Their underlying types share the same memory location.
- Thay can become raw **union**s with **@untagged** attribute (e.g., **@untagged(i32 | f32)**).
- They're normally structs with **tag: u8** (or **u16**, **u32**, **u64**), **data: @untagged(T1 | T2 | ...| TN)**.
