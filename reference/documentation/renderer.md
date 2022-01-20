---
description: renderer table
---

# Renderer

### text(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Text        | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:text(event:stack(), textOf("Ferret"), vec2d(2, 2), color(255, 255, 255, 255))
```

### text(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| string      | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:text(event:stack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
```

### textWithShadow(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| Text        | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:textWithShadow(event:stack(), textOf("Ferret"), vec2d(2, 2), color(255, 255, 255, 255))
```

### textWithShadow(stack, text, vec2d, color)

| Type        | name  |
| ----------- | ----- |
| MatrixStack | stack |
| string      | text  |
| Vec2d       | vec2d |
| Color       | color |

```lua
renderer:textWithShadow(event:stack(), "Ferret", vec2d(2, 2), color(255, 255, 255, 255))
```

### rect(stack, from, to, color)

| Type         | name  |
| ------------ | ----- |
| MatrixStackr | stack |
| Vec2d        | from  |
| Vec2d        | to    |
| Color        | color |

```lua
renderer:rect(event:stack(), vec2d(2, 2), vec2d(12, 12), color(255, 255, 255, 255))
```

### rectFilled(stack, from, to, color)

| Type         | name  |
| ------------ | ----- |
| MatrixStackr | stack |
| Vec2d        | from  |
| Vec2d        | to    |
| Color        | color |

```lua
renderer:rectFilled(event:stack(), vec2d(2, 2), vec2d(12, 12), color(255, 255, 255, 150))
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
renderer:rectFilled(event:stack(), vec2d(2, 2), vec2d(12, 12), color(255, 0, 0, 150), color(0, 0, 255, 150))
```

### line(stack, from, to, color)

| Type         | name  |
| ------------ | ----- |
| MatrixStackr | stack |
| Vec2d        | from  |
| Vec2d        | to    |
| Color        | color |

```
renderer:line(event:stack(), vec2d(2, 2), vec2d(12, 12), color(255, 255, 255, 150))
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

