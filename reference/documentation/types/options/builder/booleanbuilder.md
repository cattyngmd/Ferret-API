# BooleanBuilder

## Methods

### new(value): [_BooleanBuilder_](booleanbuilder.md)__

Constructor. Returns new BooleanBuilder.

| Type    | name  |
| ------- | ----- |
| boolean | value |

### build(feature): [_BooleanOption_](../booleanoption.md)__

Builds option and register itself in Option List.

| Type    | name    |
| ------- | ------- |
| Feature | feature |

```lua
local option = BooleanBuilder(true):name("Boolean Option"):build(feature)
```
