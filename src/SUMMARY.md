# The Protocol Verification Language Reference

[Introduction](introduction.md)

- [Build System](build-system.md)

  - [Project Structure](build-system/project-structure.md)
  - [Manifest File Format](build-system/manifest-file-format.md)
  - [Module System](build-system/module-system.md)
  - [Dependency Resolution Strategy](build-system/dependency-resolution-strategy.md)

- [Syntax and Semantics](syntax-and-semantics.md)

  - [Comments](syntax-and-semantics/comments.md)
    - [Line](syntax-and-semantics/comments/line.md)
    - [Block](syntax-and-semantics/comments/block.md)

  - [Identifiers](syntax-and-semantics/identifiers.md)

  - [Generics](syntax-and-semantics/generics.md)

  - [Paths](syntax-and-semantics/paths.md)

  - [Types](syntax-and-semantics/types.md)
    - [Primitive](syntax-and-semantics/types/primitive.md)
      - [bool](syntax-and-semantics/types/primitive/bool.md)
      - [u8](syntax-and-semantics/types/primitive/u8.md)
      - [u16](syntax-and-semantics/types/primitive/u16.md)
      - [u32](syntax-and-semantics/types/primitive/u32.md)
      - [u64](syntax-and-semantics/types/primitive/u64.md)
      - [u128](syntax-and-semantics/types/primitive/u128.md)
      - [usize](syntax-and-semantics/types/primitive/usize.md)
      - [natural](syntax-and-semantics/types/primitive/natural.md)
      - [i8](syntax-and-semantics/types/primitive/i8.md)
      - [i16](syntax-and-semantics/types/primitive/i16.md)
      - [i32](syntax-and-semantics/types/primitive/i32.md)
      - [i64](syntax-and-semantics/types/primitive/i64.md)
      - [i128](syntax-and-semantics/types/primitive/i128.md)
      - [isize](syntax-and-semantics/types/primitive/isize.md)
      - [integer](syntax-and-semantics/types/primitive/integer.md)
      - [f32](syntax-and-semantics/types/primitive/f32.md)
      - [f64](syntax-and-semantics/types/primitive/f64.md)
      - [f128](syntax-and-semantics/types/primitive/f128.md)
      - [real](syntax-and-semantics/types/primitive/real.md)
      - [decimal](syntax-and-semantics/types/primitive/decimal.md)
      - [fractional](syntax-and-semantics/types/primitive/fractional.md)
      - [imaginary](syntax-and-semantics/types/primitive/imaginary.md)
      - [char](syntax-and-semantics/types/primitive/char.md)
      - [string](syntax-and-semantics/types/primitive/string.md)
      - [duration](syntax-and-semantics/types/primitive/duration.md)
    - [Pointer](syntax-and-semantics/types/pointer.md)
    - [Reference](syntax-and-semantics/types/reference.md)
    - [Slice](syntax-and-semantics/types/slice.md)
    - [Array](syntax-and-semantics/types/array.md)
    - [Tuple](syntax-and-semantics/types/tuple.md)
    - [Struct](syntax-and-semantics/types/struct.md)
    - [Variant](syntax-and-semantics/types/variant.md)
    - [Named](syntax-and-semantics/types/named.md)
    - [Abstract](syntax-and-semantics/types/abstract.md)

  - [Patterns](syntax-and-semantics/patterns.md)
    - [Tuple](syntax-and-semantics/patterns/tuple.md)
    - [Slice](syntax-and-semantics/patterns/slice.md)
    - [Struct](syntax-and-semantics/patterns/struct.md)
    - [Type](syntax-and-semantics/patterns/type.md)

  - [Flow Control Structures](syntax-and-semantics/flow-control-structures.md)
    - [Block](syntax-and-semantics/flow-control-structures/block.md)
    - [Conditional](syntax-and-semantics/flow-control-structures/conditional.md)
    - [When](syntax-and-semantics/flow-control-structures/when.md)
    - [Infinite Loop](syntax-and-semantics/flow-control-structures/infinite-loop.md)
    - [While Loop](syntax-and-semantics/flow-control-structures/while-loop.md)
    - [For Loop](syntax-and-semantics/flow-control-structures/for-loop.md)

  - [Expressions](syntax-and-semantics/expressions.md)
    - [Literal](syntax-and-semantics/expressions/literal.md)
      - [Boolean](syntax-and-semantics/expressions/literal/boolean.md)
      - [Integer](syntax-and-semantics/expressions/literal/integer.md)
      - [Floating Point](syntax-and-semantics/expressions/literal/floating-point.md)
      - [Imaginary](syntax-and-semantics/expressions/literal/imaginary.md)
      - [Character](syntax-and-semantics/expressions/literal/character.md)
      - [String](syntax-and-semantics/expressions/literal/string.md)
      - [Duration](syntax-and-semantics/expressions/literal/duration.md)
    - [Item](syntax-and-semantics/expressions/item.md)
    - [Range](syntax-and-semantics/expressions/range.md)
    - [Array](syntax-and-semantics/expressions/array.md)
    - [Tuple](syntax-and-semantics/expressions/tuple.md)
    - [Struct](syntax-and-semantics/expressions/struct.md)
    - [Indexing](syntax-and-semantics/expressions/indexing.md)
    - [Ranged Indexing](syntax-and-semantics/expressions/ranged-indexing.md)
    - [Field Access](syntax-and-semantics/expressions/field-access.md)
    - [Call](syntax-and-semantics/expressions/call.md)
    - [Method Call](syntax-and-semantics/expressions/method-call.md)
    - [Spread](syntax-and-semantics/expressions/spread.md)
    - [Cast](syntax-and-semantics/expressions/cast.md)
    - [Unary](syntax-and-semantics/expressions/unary.md)
    - [Binary](syntax-and-semantics/expressions/binary.md)
    - [Is](syntax-and-semantics/expressions/is.md)
    - [Try](syntax-and-semantics/expressions/try.md)
    - [Lambda](syntax-and-semantics/expressions/lambda.md)
    - [Machine](syntax-and-semantics/expressions/machine.md)
    - [Trigger](syntax-and-semantics/expressions/trigger.md)
    - [Parenthesized](syntax-and-semantics/expressions/parenthesized.md)
    - [Block](syntax-and-semantics/expressions/block.md)
    - [Conditional](syntax-and-semantics/expressions/conditional.md)
    - [When](syntax-and-semantics/expressions/when.md)
    - [Infinite Loop](syntax-and-semantics/expressions/infinite-loop.md)
    - [While Loop](syntax-and-semantics/expressions/while-loop.md)
    - [For Loop](syntax-and-semantics/expressions/for-loop.md)

  - [Expression Precedence](syntax-and-semantics/expression-precedence.md)

  - [Specifications](syntax-and-semantics/specifications.md)
    - [Propositions](syntax-and-semantics/specifications/propositions.md)
    - [Assumes](syntax-and-semantics/specifications/assumes.md)
    - [Requires](syntax-and-semantics/specifications/requires.md)
    - [Ensures](syntax-and-semantics/specifications/ensures.md)

  - [Statements](syntax-and-semantics/statements.md)
    - [Import](syntax-and-semantics/statements/import.md)
    - [Export](syntax-and-semantics/statements/export.md)
    - [Alias Definition](syntax-and-semantics/statements/alias-definition.md)
    - [Type Definition](syntax-and-semantics/statements/type-definition.md)
    - [Machine Definition](syntax-and-semantics/statements/machine-definition.md)
    - [Extension Definition](syntax-and-semantics/statements/extension-definition.md)
    - [Function Definition](syntax-and-semantics/statements/function-definition.md)
    - [Test Definition](syntax-and-semantics/statements/test-definition.md)
    - [Method Definition](syntax-and-semantics/statements/method-definition.md)
    - [Operator Overload](syntax-and-semantics/statements/operator-overload.md)
    - [Interface Definition](syntax-and-semantics/statements/interface-definition.md)
    - [Constant Definition](syntax-and-semantics/statements/constant-definition.md)
    - [Static Variable Definition](syntax-and-semantics/statements/static-variable-definition.md)
    - [Local Variable Definition](syntax-and-semantics/statements/local-variable-definition.md)
    - [Expression](syntax-and-semantics/statements/expression.md)
    - [Defer](syntax-and-semantics/statements/defer.md)
    - [Return](syntax-and-semantics/statements/return.md)
    - [Break](syntax-and-semantics/statements/break.md)
    - [Continue](syntax-and-semantics/statements/continue.md)
    - [Goto](syntax-and-semantics/statements/goto.md)
    - [Assume](syntax-and-semantics/statements/assume.md)
    - [Assert](syntax-and-semantics/statements/assert.md)
    - [Block](syntax-and-semantics/statements/block.md)
    - [Conditional](syntax-and-semantics/statements/conditional.md)
    - [When](syntax-and-semantics/statements/when.md)
    - [Infinite Loop](syntax-and-semantics/statements/infinite-loop.md)
    - [While Loop](syntax-and-semantics/statements/while-loop.md)
    - [For Loop](syntax-and-semantics/statements/for-loop.md)

  - [Special Interfaces](syntax-and-semantics/special-interfaces.md)
    - [Callable](syntax-and-semantics/special-interfaces/callable.md)
    - [Range](syntax-and-semantics/special-interfaces/range.md)

  - [Special Types](syntax-and-semantics/special-types.md)
    - [Optional](syntax-and-semantics/special-types/optional.md)
    - [Result](syntax-and-semantics/special-types/result.md)

  - [Name Resolution](syntax-and-semantics/name-resolution.md)
  - [Constant Evaluation](syntax-and-semantics/constant-evaluation.md)
  - [Type Checking](syntax-and-semantics/type-checking.md)
  - [Type Inference](syntax-and-semantics/type-inference.md)

  - [Complete Grammar](syntax-and-semantics/complete-grammar.md)
