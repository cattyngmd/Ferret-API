# colors

## Methods

### rgb(red, green, blue): _color_

Creates a new color object.

| Type | name  |
| ---- | ----- |
| int  | red   |
| int  | green |
| int  | blue  |

```lua
colors.rgb(255, 0, 0) -- red
```

### rgba(red, green, blue, alpha): _color_

Creates a new color object with alpha.

| Type | name  |
| ---- | ----- |
| int  | red   |
| int  | green |
| int  | blue  |
| int  | alpha |

```lua
colors.rgb(255, 0, 0, 127) -- red with half opacity
```

### hsv(hue, saturation, brightness): _color_

Creates a new color object using hsv.

| Type  | name       |
| ----- | ---------- |
| float | hue        |
| float | saturation |
| float | brightness |

```lua
colors.rgb(120.0, 1.0, 1.0) -- green
```

### fade(color1, color2, progress): _color_

Mixes two color.

| Type  | name     |
| ----- | -------- |
| color | color1   |
| color | color2   |
| float | progress |

```lua
colors.fade(color(255, 0, 0, 255), color(0, 0, 255, 255), 0.5) -- pink
```

### rainbow(delay, saturation, brightness, alpha): _color_

Creates a new rainbow color object.

| Type  | name       |
| ----- | ---------- |
| int   | delay      |
| float | saturation |
| float | brightness |
| int   | alpha      |

```lua
color.rainbow(0, 1.0, 1.0, 255)
```

### pulse(color1, color2, time, delay): _color_

Creates a new pulse color object.

| Type  | name   |
| ----- | ------ |
| color | color1 |
| color | color2 |
| float | time   |
| int   | delay  |

```lua
color.pulse(color(255, 0, 0, 255), color(127, 0, 0, 255), 1000, 0)
```
