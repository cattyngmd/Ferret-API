# Player Move Event

## `player_move`

Dispatches on any player's move action.

### Fields

| Type         | name     |
| ------------ | -------- |
| MovementType | type     |
| Vec3d        | velocity |

### Methods

| Type         | name                |
| ------------ | ------------------- |
| MovementType | getType             |
| Vec3d        | getVelocity         |
| void         | setVelocity(vec3d)  |
| void         | setVelocityX(x)     |
| void         | setVelocityY(y)     |
| void         | setVelocityZ(z)     |
| void         | setVelocityXZ(x, z) |

### Example

```lua
-- HighJump
this:registerCallback("events", function(event)
    if (event:getName() == "player_move") then
        event:setVelocityY(event:getVelocity().y * 2)
    end
end)
```
