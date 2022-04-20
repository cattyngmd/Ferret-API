# StopWatch

## Methods

### StopWatch

Constructor.

```lua
local watch = StopWatch()
```

### passed(ms): _boolean_

Checks if timer has elapsed.

| Type | name |
| ---- | ---- |
| long | ms   |

```lua
local watch = StopWatch()

if watch:passed(1000) then
    print("1 second has elapsed!")
end
```

### reset

Resets the timer.

```lua
local watch = StopWatch()

watch:reset()
```
