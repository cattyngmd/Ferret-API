# NumberOption

## Methods

### getValue(): _double_

Returns current value of option.

```lua
local option = NumberBuilder(1):name("Number Option"):setBounds(1, 10):build(feature)
print(option:getValue()) -- 1
```

### setValue(value)

Changes current value of option.

| Type   | name  |
| ------ | ----- |
| double | value |

```lua
local option = NumberBuilder(1):name("Number Option"):setBounds(1, 10):build(feature)
option:setValue(5)
print(option:getValue()) -- 5
```

### setStringValue(value)

Same as `setValue`

| Type   | name  |
| ------ | ----- |
| string | value |

```lua
local option = NumberBuilder(1):name("Boolean Option"):setBounds(1, 10):build(feature)
option:setStringValue("6")
print(option:getValue()) -- 6
```
