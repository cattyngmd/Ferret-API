# TextOption

## Methods

### getValue(): _string_

Returns current value of option.

```lua
local option = TextBuilder("Sample Text"):name("Text Option"):build(feature)
print(option:getValue()) -- Sample Text
```

### setValue(value)

Changes current value of option.

| Type   | name  |
| ------ | ----- |
| string | value |

```lua
local option = TextBuilder("Sample Text"):name("Text Option"):build(feature)
option:setValue("Another Text")
print(option:getValue()) -- Another Text
```

### setStringValue(value)

Same as `setValue`

| Type   | name  |
| ------ | ----- |
| string | value |

```lua
local option = TextBuilder("Sample Text"):name("Text Option"):build(feature)
option:setStringValue("Another Text")
print(option:getValue()) -- Another Text
```
