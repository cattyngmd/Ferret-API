# Render 3D Event

## `render_3d`

Dispatches on every world render frame.

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

### Example

```lua
this:registerCallback("events", function(event)
    if event:getName() == "render_3d" then
        renderer:drawBoxFilled(event:getStack(), mc.player:getBlockPos(), color(255, 255, 255, 130)
    end
end)
```
