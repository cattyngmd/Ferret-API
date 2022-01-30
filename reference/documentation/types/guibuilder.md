# GuiBuilder

## Methods

### new(name): [_GuiBuilder_](guibuilder.md)__

Constructor. Creates new GuiBuilder.

| Type   | name |   |
| ------ | ---- | - |
| string | name |   |

```lua
local gui = GuiBuilder.new("Simple Gui")
```

### isPauseScreen(pause): [_GuiBuilder_](guibuilder.md)

If `true` gui will not pause screen, otherwise it will.

| Type    | name  |   |
| ------- | ----- | - |
| boolean | pause |   |

```lua
local gui = GuiBuilder.new("Simple Gui"):isPauseScreen(false)
```

### setRender(callback): [_GuiBuilder_](guibuilder.md)__

Creates callback for `render` method in Screen class.

| Type     | name     |   |
| -------- | -------- | - |
| function | callback |   |

```lua
local gui = GuiBuilder.new("Simple Gui"):setRender(function(stack, cursor)
    renderer:textWithShadow(stack, "Hello!", cursor, color(255, 255, 255, 255)
end)
```

### setKeyPressed(callback): [_GuiBuilder_](guibuilder.md)__

Creates callback for `keyPressed` method in Screen class.

| Type     | name     |   |
| -------- | -------- | - |
| function | callback |   |

```lua
local gui = GuiBuilder.new("Simple Gui"):setKeyPressed(function(key, scan, modifiers)
    print(key)
end)
```

### setKeyReleased(callback): [_GuiBuilder_](guibuilder.md)__

Creates callback for `keyReleased` method in Screen class.

| Type     | name     |   |
| -------- | -------- | - |
| function | callback |   |

```lua
local gui = GuiBuilder.new("Simple Gui"):setKeyReleased(function(key, scan, modifiers)
    print(key)
end)
```

### setMouseClicked(callback): [_GuiBuilder_](guibuilder.md)__

Creates callback for `mouseClicked` method in Screen class

| Type     | name     |   |
| -------- | -------- | - |
| function | callback |   |

```lua
local gui = GuiBuilder.new("Simple Gui"):setMouseClicked(function(cursor, key)
    print(string.format("click! x:%s y:%s", cursor:x(), cursor:y())
end)
```

### setMouseReleased(callback): [_GuiBuilder_](guibuilder.md)__

Creates callback for `mouseReleased` method in Screen class

| Type     | name     |   |
| -------- | -------- | - |
| function | callback |   |

```lua
local gui = GuiBuilder.new("Simple Gui"):setMouseReleased(function(cursor, key)
    print(string.format("x:%s y:%s", cursor:x(), cursor:y())
end)
```

### setCharTyped(callback): [_GuiBuilder_](guibuilder.md)__

Creates callback for `charTyped` method in Screen class

| Type     | name     |   |
| -------- | -------- | - |
| function | callback |   |

```lua
local text = ""
local gui = GuiBuilder.new("Simple Gui"):setRender(function(stack, cursor)
    renderer:textWithShadow(stack, text, cursor, color(255, 255, 255, 255)
end):setCharTyped(function(chr, modifiers)
    text = text .. string.char(char)
end)
```

### build(): _Screen_

Builds screen.

```lua
local gui = GuiBuilder.new("Simple Gui"):isPauseScreen(false):setRender(function(stack, cursor)
    renderer:textWithShadow(stack, "Hello!", cursor, color(255, 255, 255, 255)
end):build()
```
