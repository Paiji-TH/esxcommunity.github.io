# ESX.Game.GetClosestPlayer

This function gets the closest player.

#### Syntax

```lua
ESX.Game.GetClosestPlayer(coords)
```

##### Optional arguments
- **coords**: A table of the xyz coords.

#### Examples

##### Lua
```lua
local closestPlayer, closestDistance = ESX.Game.GetClosestPlayer()

if closestPlayer ~= -1 and closestDistance <= 3.0 then
  -- Do something..
  print('A player is nearby!')
end
```
