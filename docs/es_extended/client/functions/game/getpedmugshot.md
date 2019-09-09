# ESX.Game.GetPedMugshot

This function generates a Mugshot of the current player usable in various applications.

#### Syntax

```lua
local mugshot, mugshotStr = ESX.Game.GetPedMugshot(ped)
```

##### Required arguments
- **ped**: A int, ped

!!! warning
    Be sure to use `UnregisterPedheadshot(mugshot)` after using it, because the game only allows you to register 34 mugshots.

#### Examples

```lua
local mugshot, mugshotStr = ESX.Game.GetPedMugshot(GetPlayerPed(-1))
UnregisterPedheadshot(mugshot)
```