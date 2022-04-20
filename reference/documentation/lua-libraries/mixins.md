# Mixins

## Methods

### mixinInject(classPath, methodName, at, args, atTarget, remap, ordinal): _String_

Creates a new mixin. Returns callback name of mixin. <mark style="color:red;">**You need to restart the game to apply mixin**</mark>**.**

<table><thead><tr><th>Type</th><th>name</th><th data-type="checkbox">optional</th></tr></thead><tbody><tr><td>string</td><td>classPath</td><td>false</td></tr><tr><td>string</td><td>methodName</td><td>false</td></tr><tr><td>string</td><td>at</td><td>false</td></tr><tr><td>int</td><td>args</td><td>false</td></tr><tr><td>string</td><td>atTarget</td><td>true</td></tr><tr><td>boolean</td><td>remap</td><td>true</td></tr><tr><td>int</td><td>ordinal</td><td>true</td></tr></tbody></table>

```lua
local testMixin = this:mixinInject(
    "net.minecraft.client.Keyboard",
    "onKey",
    "HEAD",
    5
)
```

## Registering Mixins Body

To register mixin's body you need to invoke `registerCallback` method with mixin name as first argument. <mark style="color:red;">**You need to restart the game to change mixin's body**</mark>**.**

```lua
local testMixin = this:mixinInject(
    "net.minecraft.client.Keyboard",
    "onKey",
    "HEAD",
    5
)

this:registerCallback(testMixin, function(mixin)
    print("[onKey] " .. mixin.args[2]) -- args[2] = key
end)
```
