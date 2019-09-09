# ESX.Game.GetClosestObject

This function gets the closest object.

#### Syntax

```lua
ESX.Game.GetClosestObject(filter, coords)
```

##### Required arguments
- **filter**: A string or table of hash strings

##### Optional arguments
- **coords**: A table of the xyz coords

#### Examples

##### Lua
```lua
local closestObject, closestDistance = ESX.Game.GetClosestObject('prop_bench_01a')
```