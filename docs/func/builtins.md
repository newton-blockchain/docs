# Built-ins
This section describes some language constructions which are less fundamental that ones described in previous sections. They could be defined in [stdlib.fc](/func/stdlib.md), but it would leave less room for FunC optimizer.

## Throwing exceptions
Exceptions can be thrown by conditional primitives `throw_if` and `throw_unless` and by unconditional `throw`. The first argument is the error code, the second is the condition (`throw` has only one argument).

## Booleans
- `true` is alias for `-1`
- `false` is alias for `0`

## Dump variable
Variable can be dumped to debug log by `~dump` function.

## Integer operations
- `muldiv` is multiple-then-divide operation. Intermediate result is stored in 513-bit integer, so it won't overflow if the actual result fits into 257-bit integer.

## Other primitives
- `null?` checks whether the argument is `null`. By the TVM type `Null` FunC represents absence of a value of some atomic type.
- `touch` and `~touch` move a variable to the top of the stack
- `at` gets the value of component of a tuple on specified position