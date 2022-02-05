# Files

### createFile(path): _File_

Creates a new and empty file, failing if the file already exists.

| Type   | name |
| ------ | ---- |
| string | path |

```lua
files:createFile("test.txt")
```

### createDir(path): _Path_

Creates a new and empty directory, failing if the file already exists.

| Type   | name |
| ------ | ---- |
| string | path |

```lua
files:createDir("test dir")
```

### createTempFile(prefix, suffix): _File_

Creates an empty file in the default temporary-file directory.

| Type   | name   |
| ------ | ------ |
| string | prefix |
| string | suffix |

```lua
files:createTempFile("ferret", ".txt")
```

### createTempDir(name): _Path_

Creates a new directory in the default temporary-file directory.

| Type   | name |
| ------ | ---- |
| string | name |

```lua
files:createTempDir("ferret")
```

### readFileAsTable(path): _LuaTable_

Reads all lines in the file and collects them in table.

| Type   | name |
| ------ | ---- |
| string | path |

```lua
local table = files:readFileAsTable("test.txt")
```

### readFile(path): _String_

Read all lines from a file.

| Type   | name |
| ------ | ---- |
| string | path |

```lua
local table = files:readFile("test.txt")
```

### writeFile(path, content)

Writes text to a file.

| Type   | name    |
| ------ | ------- |
| string | content |

```lua
files:writeFile("test.txt", "hello")
```

### writeFile(path, bytes)

Writes bytes to a file.

| Type    | name  |
| ------- | ----- |
| byte\[] | bytes |

### walk(path, closure)

| Type       | name    |
| ---------- | ------- |
| string     | path    |
| LuaClosure | closure |

```lua
files:walk("directory", function(path)
    print(tostring(path))
end)
```

### walkTree(path, closure)

| Type       | name    |
| ---------- | ------- |
| string     | path    |
| LuaClosure | closure |

```lua
files:walkTree("directory", function(path)
    print(tostring(path))
end)
```
