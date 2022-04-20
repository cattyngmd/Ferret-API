# Interactions

### canBreak(pos, state): _boolean_

Returns true if u can break block.

| Type       | name  |
| ---------- | ----- |
| BlockPos   | pos   |
| BlockState | state |

```lua
local pos = mc.player:getBlockPos():south()
if interactions:canBreak(pos, mc.world:getBlockState(pos)) then
    print("true")
end
```

### isPlaceable(pos, checkentity): _boolean_

Returns true if u can place block.

| Type     | name        |
| -------- | ----------- |
| BlockPos | pos         |
| boolean  | checkentity |

```lua
local pos = mc.player:getBlockPos():down()
if interactions:isPlaceable(pos, false) then
    interactions:place(pos, true)
end
```

### breakBlock(pos): _boolean_

Returns true if u can break block and breaks it.

| Type     | name |
| -------- | ---- |
| BlockPos | pos  |

```lua
local pos = mc.player:getBlockPos():up()
interactions:breakBlock(pos)
```

### useItem(pos)

Uses item on block.

| Type     | name |
| -------- | ---- |
| BlockPos | pos  |

```lua
local pos = mc.player:getBlockPos():up()
interactions:useItem(pos)
```

### useItem(pos, hand)

Uses item on block.

| Type     | name |
| -------- | ---- |
| BlockPos | pos  |
| Hand     | hand |

```lua
local pos = mc.player:getBlockPos():up()
interactions:useItem(pos, mc.player:getActiveHand())
```

### place(pos, airplace): _boolean_

Returns true if u can place block and places it.

| Type     | name     |
| -------- | -------- |
| BlockPos | pos      |
| boolean  | airplace |

```lua
local pos = mc.player:getBlockPos():down()
interactions:place(pos, true)
```

### place(pos, airplace, hand): _boolean_

Returns true if u can place block and places it.

| Type     | name     |
| -------- | -------- |
| BlockPos | pos      |
| boolean  | airplace |
| Hand     | hand     |

```lua
local pos = mc.player:getBlockPos():down()
interactions:place(pos, true, mc.player:getActiveHand())
```

### calcSide(pos): _Direction_

Returns the side of the neighbor block.

| Type     | name |
| -------- | ---- |
| BlockPos | pos  |

```lua
local pos = mc.player:getBlockPos():down()
print(tostring(interactions:calcSide(pos)))
```

### getBlockBreakingSpeed(slot, pos): _double_

Returns block's breaking speed.

| Type     | name |
| -------- | ---- |
| int      | slot |
| BlockPos | pos  |

```lua
local pos = mc.player:getBlockPos():down()
print(getBlockBreakingSpeed(mc.player:getInventory():selectedSlot, pos))
```

### getBlockBreakingSpeed(slot, state): _double_

Returns block's breaking speed.

| Type       | name  |
| ---------- | ----- |
| int        | slot  |
| BlockState | state |

```lua
local pos = mc.player:getBlockPos():down()
print(getBlockBreakingSpeed(mc.player:getInventory():selectedSlot, mc.world:getBlockState(pos)))
```

### right(dir): _Direction_

| Type      | name |
| --------- | ---- |
| Direction | dir  |

```lua
print(tostring(interactions:right(Direction.NORTH))) -- East
```

### left(dir): _Direction_

| Type      | name |
| --------- | ---- |
| Direction | dir  |

```lua
print(tostring(interactions:left(Direction.NORTH))) -- West
```
