# BooleanOption

## Methods

### getValue(): _boolean_

Returns current value of option.

```lua
local option = BooleanBuilder(true):name("Boolean Option"):build(feature)
print(option:getValue()) -- true
```

### setValue(value)

Changes current value of option.

| Type    | name  |
| ------- | ----- |
| boolean | value |

```lua
local option = BooleanBuilder(true):name("Boolean Option"):build(feature)
option:setValue(false)
print(option:getValue()) -- false
```

### setStringValue(value)

Parses given string value to boolean and changes current value of option.

| Type                                                                            | name  |
| ------------------------------------------------------------------------------- | ----- |
| stringlocal option = BooleanBuilder(true):name("Boolean Option"):build(feature) | value |

```lua
local option = BooleanBuilder(true):name("Boolean Option"):build(feature)
option:setValue("false")
print(option:getValue()) -- false
```
