# Post

## `render_3d_post`

Dispatches on every world render frame (after all).

### Example

```lua
this:registerCallback("events", function(event)
    if event:getName() == "render_3d_post" then
        renderer:drawBox(event:getStack(), mc.player:getBlockPos(), color(255, 255, 255, 130), 1.0)
    end
end)
```
