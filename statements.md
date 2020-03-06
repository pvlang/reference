# Statements

${...} notation means there will be a ... in here.

## Constant definition statement

```
const NAME: Type = ${constant_expression};
```

## Defer statement

```
defer ${expression};
```

## Export statement

```
export {
    project::{
        module1::{
            submodule1::{
                item1,
            },
            item2,
        },
        module2::{
            item3,
        },
        item4,
    },
};
```

## Expression statement

```
${expression};
```

## Extension definition statement

```
default extension of Type = {
    public: {
        ...
    },
    private: {
        ...
    },
};
```

```
Named extension of Type = {
    public: {
        ...
    },
    private: {
        ...
    },
};
```

## Function definition statement

```
fn name() = ${expression};
```

```
fn name(): Type = ${expression};
```

```
fn name(parameter1: Type1, parameter2: Type2, ..., parameterN: TypeN) = ${expression};
```

```
fn name(parameter1: Type1, parameter2: Type2, ..., parameterN: TypeN): Type = ${expression};
```

## Import statement

```
export {
    project1::{
        module1::{
            submodule1::{
                item1,
            },
            item2,
        },
        module2::{
            item3,
        },
        item4,
    },
    project2::{
        module1::{
            submodule1::{
                item5,
            },
            item6,
        },
        module2::{
            item7,
        },
        item8,
    },
};
```

## Local variable definition statement

```
let variable1;
```

```
let mut variable2;
```

```
let variable3 = ${expression};
```

```
let mut variable4 = ${expression};
```

```
let variable5: Type;
```

```
let mut variable6: Type;
```

```
let variable7: Type = ${expression};
```

```
let mut variable8: Type = ${expression};
```

## Method definition statement

Can only be inside of an extension definition.
Basically the same with function definition except the first argument is one of the following: `self` `&self` `&mut self`

e.g.
```
fn method1(self): i32 = self.some_integer_field + 1;
```

## Return statement

```
return ${expression};
```

```
return' ${expression};
```

```
return'' ${expression};
```

Primes are used for representing lexical scoped return.
So `return` means return to the caller, `return'` means return to 1 lexical scope up, `return''` means return to 2 lexical scopes up.

e.g.
```
for i in [1..4) {
    for j in [2..5) {
        for k in [3..6) {
            return'';
               |
        }      | // 1st lexical scope
    }          | // 2nd lexical scope
    // So code will continue from here
}
```

## Static variable definition statement

```
static STATIC1: Type;
```

```
static mut STATIC2: Type;
```

```
static STATIC3: Type = CE;
```

```
static mut STATIC4: Type = CE;
```

## Type definition statement

```
type Unit;
```

```
type Struct = {};
type Struct = { field1: Type, field2: Type, ... };
```

```
type NamedTuple = ();
type NamedTuple = (Type1, Type2, Type3, ...);
```

```
type Variant = (Type1 | Type2 | Type3);
type Variant = (
    | ExistingType1
    | type NewType
    | type AnotherNewType
    | ExistingType2
);
```
