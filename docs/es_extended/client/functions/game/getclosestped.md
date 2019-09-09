# ESX.Game.GetClosestPed

This function gets the closest ped.

#### Syntax

```lua
ESX.Game.GetClosestPed(coords, ignoreList)
```

##### Required arguments
- **coords**: A table of the xyz coords

##### Optional arguments
- **ignoreList**: A table of peds to ignore

#### Examples

##### Lua
```lua
local closestPed, closestDistance = ESX.Game.GetClosestPed()
```