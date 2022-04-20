# CommandContainer

## Methods

### executes(function): [_CommandContainer_](commandcontainer.md)__

Invokes on command execution.

| Type       | name     |
| ---------- | -------- |
| LuaClosure | function |

```lua
builder:executes(function(context)
    print("hello world")
end)
```

### next(container): [_CommandContainer_](commandcontainer.md)__

Adds a new child to the parent container.

| Type             | name      |
| ---------------- | --------- |
| CommandContainer | container |

```lua
builder:next(
    Command.BOOLEAN:create("value")
)
```

### suggest(table): [_CommandContainer_](commandcontainer.md)__

Suggests possible values for the container.

| Type     | name  |
| -------- | ----- |
| LuaTable | table |

```lua
builder:next(
    Command.STRING:create("action"):suggest(
        {"attack", "interact", "jump", "sprint", "shift"}
    )
)
```
