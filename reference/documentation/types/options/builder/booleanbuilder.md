# BooleanBuilder

## Methods

### new(value): _[_BooleanBuilder_](booleanbuilder.md)_

Constructor. Returns new BooleanBuilder.

| Type    | name  |
| ------- | ----- |
| boolean | value |

### build(feature): _[_BooleanOption_](../booleanoption.md)_

Builds option and register itself in Option List.

| Type    | name    |
| ------- | ------- |
| Feature | feature |

```lua
local option = BooleanBuilder(true):name("Boolean Option"):build(feature)
```
