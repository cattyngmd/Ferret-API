# renderer

### text(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Text        | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:text(event:getStack(), textOf("Ferret"), vec2d(2, 2), color(255, 255, 255, 255))
```

### text(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| string      | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:text(event:getStack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
```

### textWithShadow(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Text        | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:textWithShadow(event:getStack(), textOf("Ferret"), vec2d(2, 2), color(255, 255, 255, 255))
```

### textWithShadow(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| string      | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:textWithShadow(event:getStack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
```

### rect(stack, from, to, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Vec2d       | from  |
| Vec2d       | to    |
| Color       | color |

```lua
renderer:rect(event:getStack(), vec2d(2, 2), vec2d(12, 12), color(255, 255, 255, 255))
```

### rectFilled(stack, from, to, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Vec2d       | from  |
| Vec2d       | to    |
| Color       | color |

```lua
renderer:rectFilled(event:getStack(), vec2d(2, 2), vec2d(12, 12), color(255, 255, 255, 150))
```

### rectFilledFade(stack, from, to, color1, color2)

| Type         | name   |
| ------------ | ------ |
| MatrixStackr | stack  |
| Vec2d        | from   |
| Vec2d        | to     |
| Color        | color1 |
| Color        | color2 |

```lua
renderer:rectFilledFade(event:getStack(), vec2d(2, 2), vec2d(12, 12), color(255, 0, 0, 150), color(0, 0, 255, 150))
```

### line(stack, from, to, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Vec2d       | from  |
| Vec2d       | to    |
| Color       | color |

```
renderer:line(event:getStack(), vec2d(2, 2), vec2d(12, 12), color(255, 255, 255, 150))
```

### width(text): _int_

| Type   | name |
| ------ | ---- |
| string | text |

```lua
local textWidth = renderer:width("oi oi") --> 20
```

### width(text): _int_

| Type | name |
| ---- | ---- |
| Text | text |

```lua
local textWidth = renderer:width(textOf("oi oi")) --> 20
```

### drawBoxFilled(stack, box, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Box         | box   |
| Color       | color |

```lua
renderer:drawBoxFilled(event:getStack(), box, color(255, 255, 255, 255))
```

### drawBoxFilled(stack, pos, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| BlockPos    | pos   |
| Color       | color |

```lua
renderer:drawBoxFilled(event:getStack(), pos, color(255, 255, 255, 255))
```

### drawBoxFilled(stack, vec3d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Vec3d       | vec3d |
| Color       | color |

```lua
renderer:drawBoxFilled(event:getStack(), vec3d(0, 64, 0), color(255, 255, 255, 255))
```

### drawBox(stack, box, color, lineWidth)

| Type        | name      |
| ----------- | --------- |
| MatrixStack | stack     |
| Box         | box       |
| Color       | color     |
| double      | lineWidth |

```lua
renderer:drawBox(event:getStack(), box, color(255, 255, 255, 255), 1.0)
```

### drawBox(stack, pos, color, lineWidth)

| Type        | name      |
| ----------- | --------- |
| MatrixStack | stack     |
| BlockPos    | pos       |
| Color       | color     |
| double      | lineWidth |

```lua
renderer:drawBox(event:getStack(), pos, color(255, 255, 255, 255), 1.0)
```

### drawBox(stack, vec3d, color, lineWidth)

| Type        | name      |
| ----------- | --------- |
| MatrixStack | stack     |
| Vec3d       | vec3d     |
| Color       | color     |
| double      | lineWidth |

```lua
renderer:drawBox(event:getStack(), vec3d(0, 64, 0), color(255, 255, 255, 255), 1.0)
```

### drawSemi2dRect(pos, offset1, offset2, scale, color)

| Type   | name    |
| ------ | ------- |
| Vec3d  | pos     |
| Vec2d  | offset1 |
| Vec2d  | offset2 |
| double | scale   |
| Color  | color   |

```lua
renderer:drawSemi2dRect(vec3d(0, 64, 0), vec2d(0, 0), vec2d(20, 5), 1.0, color(255, 255, 255, 255))
```

### drawSemi2dText(text, pos, offset, scale, color, shadow)

| Type    | name    |
| ------- | ------- |
| string  | text    |
| Vec3d   | pos     |
| Vec2d   | offset1 |
| Vec2d   | offset2 |
| double  | scale   |
| Color   | color   |
| boolean | shadow  |

```lua
renderer:drawSemi2dText("Hello", vec3d(0, 64, 0), vec2d(0, 0), vec2d(0, 0), 1.0, color(255, 255, 255, 255), true)
```

### setup()

```
renderer:setup()
```

### setup3D()

```
renderer:setup3D()
```

### clean()

```
renderer:clean()
```

### clean3D()

```
renderer:clean3D()
```
