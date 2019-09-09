# ESX.Game.GetVehicleInDirection.md

This function gets the closest vehicle in the players direction within 5 units, utilizes ray-casts.

#### Syntax

```lua
ESX.Game.GetVehicleInDirection()
```

#### Examples

#### Lua
```lua
local vehicle = ESX.Game.GetVehicleInDirection()

if DoesEntityExist(vehicle) then
  -- Vehicle found do something..
end
```
