# ModuleLua

## Methods

### new(name, desc, category, script): [_ModuleLua_](modulelua.md)__

Constructor. Creates Module but doesnt register callbacks and itself in ModuleManager.

| Type   | name        |
| ------ | ----------- |
| string | name        |
| string | description |
| string | category    |
| Script | script      |

```lua
local module = Module.new("TestModule", "Funny", "PLAYER", this)
```

### body(function)

Creates body of the module. Also register itself in ModuleManager.

| Type       | name     |
| ---------- | -------- |
| LuaClosure | function |

```lua
-- Simple Sprint Module
local module = Module.new("SprintLua", "You run faster", "MOVEMENT", this)

module:body(function()

     local omni = BooleanBuilder(false):name("Rage"):build(module)
     
     module:registerCallback("events", function(event)
          if(event:getName() == "tick") then
               if mc.player.forwardSpeed > 0 or omni:getValue() then
                    mc.player:setSprinting(true)
               end
          end
     end)
     
end)
```

### onEnable(function)

Overrides onEnable method.

| Type       | name     |
| ---------- | -------- |
| LuaClosure | function |

```lua
local module = Module.new("Test", "", "PLAYER", this)

module:onEnable(function()
    print(module:getName() .. " enabled!")
end)
```

### onDisable(function)

Overrides onDisable method.

| Type       | name     |
| ---------- | -------- |
| LuaClosure | function |

```lua
local module = Module.new("Test", "", "PLAYER", this)

module:onEnable(function()
    print(module:getName() .. " enabled!")
end)
```

### registerCallback(name, function)

Creates new callback for Module.

| Type        | name     |
| ----------- | -------- |
| string      | name     |
| LuaFunction | function |

```lua
local module = Module.new("TestModule", "Test", "VISUAL", this)

module:body(function()

    module:registerCallback("hud", function(arg)
        renderer:text(hud:getStack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
    end)

end)
```

### register()

Register Modules callbacks and itself in ModuleManager.

```lua
local module = Module.new("TestModule", "Test", "VISUAL", this)
module:register()
```
