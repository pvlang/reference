# Types

## Nothing type

It's like `void` in C.
It has the size of 0, and it is used as a marker.

- nothing

## Boolean type

Can be either `true` or `false`.
Its representation in memory is not required to be `true == 1`, `false == 0`.

- bool

## Signed integer types

Represented with _Two's Complement_ in the memory.
They start with **i** and end with the bit width of type (eg. `i32` is 32-bit wide integer with _Two's Complement_ representation).
`isize` is a signed integer type with the size of the machine word.

- i8
- i16
- i32
- i64
- i128
- isize

## Unsigned integer types

They start with **u** and end with the bit width of type (eg. `u32` is 32-bit wide unsigned integer).
`usize` is an unsigned integer type with the size of the machine word.

- u8
- u16
- u32
- u64
- u128
- usize

## Floating-point types

Represented in IEEE 754 standard in memory.

- f32
- f64
- f128

## Char type

1 byte of ASCII encoded character.
Basically `i8`.

- char

## String type

Always valid UTF-8 encoded sequence of bytes.
Basically `{ buffer: *u8, length: usize }`
Buffer is not owned.

- string

## Pointer types

- *T
- *mut T

## Reference types

- &T
- &mut T

## Slice types

Basically `{ buffer: *T, length: usize }`
Buffer is not owned.

- [T]
- [mut T]

## Range type

Can be bounded or unbounded with inclusive and exclusive bounds.
`T` cannot be a range type.

- ..T..

## Array type

A stack-allocated array of `T` with _constant-expression_ elements inside.
`CE` stands for **Constant Expression**.

- [T <| CE]

## Tuple type

Act like anonymous structs with the fields `0, 1, ..., n`.
`()` a.k.a. empty tuple is also a valid type, and it has a size of 0 just like the nothing type.
`CE` stands for **Constant Expression**.

- (T1, T2, ..., TN)
- (T <| CE)

## Struct type

If two struct has the same field names and same types corresponding to field names, they are considered the same.

- { field1: T1, field2: T2, ..., fieldN: TN }

## Variant type

Basically, an enumeration type consisting of types rather than enumeration constants.
Mapped to a struct containing an enum for the tag and a union for possible data.

- (T1 | T2 | ... | TN)

## User-defined types

Types defined with `type Name = ...;` statements.
Can have a path (eg. std::foo::Bar).

- Name

## Generic types

Types defined with `type Name[...] = ...;` statements.
Generic parameters can be types, literals or constant expressions with a `$` in the beginning.
Can have a path before the name (eg. std::foo::Bar).

- Name[T1, T2, L1, L2, $CE1, $CE2]
