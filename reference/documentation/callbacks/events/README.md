# Events

## `events`

Dispatches on every event

### Fields

| Type    | name      |
| ------- | --------- |
| boolean | cancelled |

### Methods

| Type     | name                    |
| -------- | ----------------------- |
| boolean  | isCancelled             |
| void     | setCancelled(cancelled) |
| void     | cancel                  |
| string   | getName                 |
| LuaValue | toLua                   |

```lua
this:registerCallback("events", function(event)
    print(event:getName())
end)
```
