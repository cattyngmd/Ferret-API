# Pre

## `render_3d_pre`

Dispatches on every world render frame (before entity render).

### Example

```lua
this:registerCallback("events", function(event)
    if event:getName() == "render_3d_pre" then
        renderer:drawBoxFilled(event:getStack(), mc.player:getBlockPos(), color(255, 255, 255, 130))
    end
end)
```
