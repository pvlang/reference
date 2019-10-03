# Types

This document does not describe how to define your own types.
Rather, it describes what can a type of variable be or what a function may return.

## Nothing type

This type is like `void` in C. It has the size of 0 and used as a marker.

- nothing

## Boolean type

It can be either `true` or `false`.
Internal representation is not required to be `true == 1`, `false == 0`.

- bool

## Signed integer types

Represented in _Two's complement_ form in memory.
They start with **i** and end with the bit width of type (eg. `i32` is 32-bit wide integer in _Two's complement_ form).

- i8
- i16
- i32
- i64
- isize

## Unsigned integer types

They start with **u** and end with the bit width of type (eg. `u32` is 32-bit wide unsigned integer).

- u8
- u16
- u32
- u64
- usize

## Floating-point types

Represented in IEEE 754 standard in memory.

- f32
- f64

## Char type

1 byte of ASCII encoded character.
Basically `i8`.

- char

## String type

Always valid UTF-8 encoded sequence of bytes.
Basically `{ ptr: &u8, length: usize }`

- string

## Pointer types

They are like pointers in C.
No guarantees about the validity.

- &T
- &mut T

## Range type

It can be bounded or unbounded with inclusive and exclusive bounds.

- ..T..

## Array type

A stack-allocated array of **T** with _constant-expression_ elements inside.

- [T <| _constant-expression_]

## Tuple type

Act like anonymous structs with the fields `0, 1, ..., n`.
`()` a.k.a. empty tuple is also a valid type, and it has a size of 0.

- (T1, T2, ..., TN)
- (T <| _constant-expression_)

## Struct type

If two struct has the same field names and same types corresponding to field names, they are considered the same.

- { field1: T1, field2: T2, ..., fieldN: TN }

## Variant type

Basically, an enumeration type consisting of types rather than enumeration constants.
Mapped to a struct containing a variant and a union for possible data.

- (T1 | T2 | ... | TN)

## Function type

It has two components: inputs and output.
Inputs are a tuple containing the expected arguments.
The output is the type of the return value of the function.

- (T1, T2, ..., TN) -> TO
- (T <| _constant-expression_) -> TO

## User-defined types

Types defined with `type Name = ...` statements.
Can have a path before the name (eg. std::foo::Bar).

- Name

## Generic types

Types defined with `@generic(...)` and then `type Name[...] = ...` statements.
Generic parameters can be types or expressions.
Can have a path before the name (eg. std::foo::Bar).

- Name[T1, E1, T2, E2, ..., TN, EN]
