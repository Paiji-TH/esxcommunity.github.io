# ESX.Game.Utils.DrawText3D

This function draws 3D text at the specified coordinates.

#### Syntax

```lua
ESX.Game.Utils.DrawText3D(coords, text, size)
```

##### Required arguments
- **coords**: A table of the xyz coords
- **text**: A string

##### Optional arguments
- **size**: A int, if not defined it will be 1 by default

#### Examples

##### Lua
```lua
ESX.Game.Utils.DrawText3D({x = 1, y = 1, z = 1}, 'Hello', 0.6)
```
