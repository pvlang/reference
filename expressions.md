# Expressions

## Literals

### Nothing literal

- nothing

### Boolean literals

- true
- false

### Integer literals

All integer literals can include an optional type hint at the end.
Possible type hints are the name of the primitive integer types (eg. `0u8` is an unsigned integer literal with 8-bit width).

- Binary literals: `0b _? ([BINARY_DIGIT] _?)* [BINARY_DIGIT] (_? [INTEGER_TYPE_HINT])?`

- Octal literals: `0o _? ([OCTAL_DIGIT] _?)* [OCTAL_DIGIT] (_? [INTEGER_TYPE_HINT])?`

- Decimal literals: `([DECIMAL_DIGIT] _?)* [DECIMAL_DIGIT] (_? [INTEGER_TYPE_HINT])?`

- Hexadecimal literals: `0x _? ([HEXADECIMAL_DIGIT] _?)* [HEXADECIMAL_DIGIT] (_? [INTEGER_TYPE_HINT])?`

where

- [BINARY_DIGIT] = [0..1]
- [OCTAL_DIGIT] = [0..7]
- [DECIMAL_DIGIT] = [0..9]
- [HEXADECIMAL_DIGIT] = [0..9 | A..F | a..f]

There are no negative integer literals.

### Floating point literals

All floating point literals can include an optional type hint at the end.
Possible type hints are the name of the primitive floating point types (eg. `1.0f32` is an IEEE 754 encoded 32-bit wide floating point number).

- With dot: `[DECIMAL_LITERAL] . [DECIMAL_LITERAL] (_? (e | E) (+ | -)? [DECIMAL_LITERAL])? (_? [FLOATING_POINT_TYPE_HINT])?`

- With exponent: `[DECIMAL_LITERAL] _? (e | E) (+ | -)? [DECIMAL_LITERAL]? (_? [FLOATING_POINT_TYPE_HINT])?`

- With type hint: `[DECIMAL_LITERAL] _? [FLOATING_POINT_TYPE_HINT]`

### Char literals

TODO

### String literals

TODO

### Duration literals

- 10000ns
- 1000ms
- 100s
- 10m
- 1h

## Range expression

In all cases, E1 and E2 represents the lower and upper bounds respectively.
They can also be empty.

### Inclusive-Inclusive range expression

- [E1..E2]

### Inclusive-Exclusive range expression

- [E1..E2)

### Exclusive-Inclusive range expression

- (E1..E2]

### Exclusive-Exclusive range expression

- (E1..E2)

## Array expression

### Full array expression

Every expression inside the full array expression must be of the same type.

- [E1, E2, ..., EN]

### Repeating array expression

`E1` is repeated `CE` times.

- [E <| CE]

## Tuple expression

### Full tuple expression

- (E1, E2, ..., EN)

### Repeating tuple expression

`E1` is repeated `CE` times.

- (E <| CE)

## Anonymous struct expression

- @ { field1: E1, field2: E2, ..., fieldN: EN, ...E }

## Lambda expression

Used to define anonymous functions that capture their environment.

- \\= E
- \\{ ... }
- \\id1, id2, ..., idN = E
- \\id1, id2, ..., idN { ... }
- \\id1: T1, id2: T2, ..., idN: TN = E
- \\id1: T1, id2: T2, ..., idN: TN { ... }

- \\=> T = E
- \\=> T { ... }
- \\id1, id2, ..., idN => T = E
- \\id1, id2, ..., idN => T { ... }
- \\id1: T1, id2: T2, ..., idN: TN => T = E
- \\id1: T1, id2: T2, ..., idN: TN => T { ... }

## Named type expression

All named types can have a path before the type name.
Paths are identifiers separated by `::`

### For unit types

- Name

### For tuple types

- Name (E1, E2, ..., EN)

### For struct types

- Name { field1: E1, field2: E2, ..., fieldN: EN }

Or with the shorthand init syntax:

- Name { field1: E1, field2: E2, ..., fieldN: EN, ...ERest }

## Spread expression

Used to expand the tuple.
Basically it converts `(E1, E2, ..., EN)` into `E1, E2, ..., EN`.

- ..._tuple-expression_

## Binary expression

- E1 = E2

- E1 + E2
- E1 += E2

- E1 - E2
- E1 -= E2

- E1 * E2
- E1 *= E2

- E1 / E2
- E1 /= E2

- E1 % E2
- E1 %= E2

- E1 ** E2
- E1 **= E2

- E1 & E2
- E1 &= E2

- E1 | E2
- E1 |= E2

- E1 ^ E2
- E1 ^= E2

- E1 << E2
- E1 <<= E2

- E1 >> E2
- E1 >>= E2

- E1 == E2
- E1 != E2
- E1 ~= E2

- E1 < E2
- E1 <= E2

- E1 > E2
- E1 >= E2

- E1 && E2
- E1 || E2

## Unary expression

- -E
- !E
- &E
- &mut E
- *E

## Indexing expression

- E1[E2]

## Ranged Indexing expression

- TODO

## Field access expression

- E.field

## Field access expression using a pointer type

- E->field

## Tuple field access expression

- E.0
- E.1
- ...
- E.N

## Call expression

All call expressions can have a path before the function name.
Paths are identifiers separated by `::`

- name(E1, E2, ..., EN)

## Method call expression

- E.name(E1, E2, ..., EN)

## Method call expression using a pointer type

- E->name(E1, E2, ..., EN)

## Try expression

- try E

## Block expression

- { (_statement_)* E? }

## Conditional expression

- if E _block_expression_
  (else if E _block_expression_)*
  (else _block_expression_)?

## When expression

- when EXPRESSION (as IDENTIFIER)? is {
    (
      ((not)? in EXPRESSION | EXPRESSION | #PATTERN) ( or ((not)? in EXPRESSION | EXPRESSION | #PATTERN) )* ((provided EXPRESSION))? |> EXPRESSION ,
      some IDENTIFIER ((provided EXPRESSION))? |> EXPRESSION ,
      _ ((provided EXPRESSION))? |> EXPRESSION ,
    )*
  }

where PATTERN can be

- { ... } {  }
- (...) {  }
- [...] {  }
- TYPE_NAME {  }
- TYPE_NAME ... {  }

## Loop expression

- loop _block_expression_

## While expression

- while E _block_expression_

## For expression

- for IDENTIFIER in EXPRESSION

## Is expression

- E (as IDENTIFIER)? is (#PATTERN | (not)? in EXPRESSION)

## Casting expression

- (# T) E

## Parenthesized expression

- (E)
