# CommandLua

## Methods

### new(name, description, script): [_CommandLua_](./)__

Constructor. Creates new CommandLua.

| Type   | name        |   |
| ------ | ----------- | - |
| string | name        |   |
| string | description |   |
| Script | script      |   |

```lua
local notify = Command.new("notify", "sends local chat message", this)
```

### body(function)

Creates body of the command. Also register itself in CommandManager.

| Type                                        | name     |   |
| ------------------------------------------- | -------- | - |
| LuaClosure ([builder](commandcontainer.md)) | function |   |

```lua
-- notify command
local notify = Command.new("notify", "sends local chat message", this)

notify:body(function(builder) -- builder is a CommandContainer
    builder:next(
        Command.GREEDYSTRING:create("message"):executes(function(context)
            local message = Command.GREEDYSTRING:get(context, "message")
            mc.inGameHud:getChatHud():addMessage(textOf("§f[§bFerret§f]§r " .. message));
        end)
    )
end)
```

