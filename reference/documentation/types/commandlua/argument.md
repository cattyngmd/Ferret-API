# Argument

## Constants

| Type    | name         |
| ------- | ------------ |
| nil     | EMPTY        |
| string  | STRING       |
| string  | GREEDYSTRING |
| boolean | BOOLEAN      |
| int     | INTEGER      |
| double  | DOUBLE       |
| float   | FLOAT        |
| Module  | MODULE       |
| Script  | SCRIPT       |
| string  | PLAYER       |

## Methods

### get(context, name): [_CommandContainer_](commandcontainer.md)__

Gets argument value by name and context.

| Type           | name    |
| -------------- | ------- |
| CommandContext | context |
| string         | name    |

```lua
Command.BOOLEAN:create("value"):executes(function(context)
    local val = Command.BOOLEAN:get(context, "value")
end)
```

### createLiteral(name): [_CommandContainer_](commandcontainer.md)__

Creates new literal argument.

| Type   | name |
| ------ | ---- |
| string | name |

```lua
builder:next(
    Command.EMPTY:createLiteral("attack"):executes(function(context)
        --attack code block
    end)
):next(
    Command.EMPTY:createLiteral("interact"):executes(function(context)
        --interact code block
    end)
):next(
    Command.EMPTY:createLiteral("jump"):executes(function(context)
        --jump code block
    end)
)
```

### create(name): [_CommandContainer_](commandcontainer.md)__

Creates new argument.

| Type   | name |
| ------ | ---- |
| string | name |

```lua
Command.INTEGER:create("value")
```
