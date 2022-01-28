# Hud

## `hud`

Callback for render stuff in your hud.

### Fields

| Type        | name      |
| ----------- | --------- |
| MatrixStack | stack     |
| float       | tickDelta |

### Methods

| Type        | name     |
| ----------- | -------- |
| MatrixStack | getStack |
| float       | getDelta |

### Examples

```lua
-- simple watermark
this:registerCallback("hud", function(hud)
    renderer:text(hud:getStack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
end)
```

or

```lua
-- simple watermark
this:registerCallback("events", function(event)
    if(event:getName() == "render_2d") then
        renderer:text(hud:getStack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
    end
end)
```

&#x20;
