# ComboBuilder

## Methods

### new(value): [_ComboBuilder_](combobuilder.md)__

Constructor. Returns new ComboBuilder.

| Type   | name  |
| ------ | ----- |
| string | value |

### setCombo(combo...): [_ComboBuilder_](combobuilder.md) __&#x20;

Sets combo for Builder.

| Type      | name  |
| --------- | ----- |
| string... | combo |

```lua
local builder = ComboBuilder("First"):setCombo("First", "Second")
```

### build(feature): [_ComboBuilder_](combobuilder.md)__

Builds option and register itself in Option List.

| Type    | name    |
| ------- | ------- |
| Feature | feature |

```lua
local option = ComboBuilder("First"):setCombo("First", "Second"):name("Combo Option"):build(feature)
```
