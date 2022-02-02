---
description: globals table
---

# Globals

### getFps(): _int_

```lua
local currentFps = globals:getFps()
```

### getFrametime(): _double_

Returns delta time between frames.

```lua
local frametime = globals:getFrametime() -- getFrametime equals 1.0 / getFps
```

### getPosition(): [_Vec3d_](types/vec3d.md)__

Returns current player's position.

```lua
local position = globals:getPosition()
```

### currentTime(): _long_

Returns current time in ms.

```lua
local time = globals:currentTime()
```

### getServer(): _string_&#x20;

Returns current server. If server is null then it returns _"none"._

```lua
local serverIp = globals:getServer()
```

### getUsername(): _string_

Returns player's username.

```lua
local myIgn = globals:getUsername()
```

### getTickMultiplier(): _float_

Returns current tickLength multiplier.

```lua
local timer = globals:getTickMultiplier()
```

### setTickMultiplier(multiplier)

| Type  | Name       |
| ----- | ---------- |
| float | multiplier |

Sets the float value of tickLength multiplier.

```lua
globals:setTickMultiplier(2.0)
```

### getEntities(): _List\<Entit_y_>_

Returns list of entities in the world.

```lua
local entities = globals:getEntities()

-- in loop
for i = 0, entities:size() - 1 do
    print(entities:get(i):getEntityName())
end
```
