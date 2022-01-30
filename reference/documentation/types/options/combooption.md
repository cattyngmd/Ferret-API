# ComboOption

## Methods

### getValue(): _string_

Returns current value of option.

```lua
local option = ComboBuilder("First"):name("Combo Option"):setCombo("First", "Second"):build(feature)
print(option:getValue()) -- First
```

### setValue(value)

Changes current value of option.

| Type   | name  |
| ------ | ----- |
| string | value |

```lua
local option = ComboBuilder("First"):name("Combo Option"):setCombo("First", "Second"):build(feature)
option:setValue("Second")
print(option:getValue()) -- Second
```

### setStringValue(value)

Same as `setValue`

| Type   | name  |
| ------ | ----- |
| string | value |

```lua
local option = ComboBuilder("First"):name("Combo Option"):setCombo("First", "Second"):build(feature)
option:setStringValue("Second")
print(option:getValue()) -- Second
```
