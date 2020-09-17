# `duration` Type

## Syntax

```
<duration-type> ::= "duration"
```

## Semantics

- It's basically a struct with **seconds: u64** and **nanoseconds: u32**.
- It's **nanoseconds** field is never bigger than 10<sup>9</sup>.
- It can hold more than 584942417355 years!
