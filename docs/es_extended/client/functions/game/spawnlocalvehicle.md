# ESX.Game.SpawnLocalVehicle

This function spawns a local vehicle, only visible to the local player and no one else.

#### Syntax

```lua
ESX.Game.SpawnLocalVehicle(modelOrHash, coords, heading, cb)
```

##### Required arguments
- **modelOrHash**: Vehicle model or hash of the model.
- **coords**: A table that contains xyz coords where the vehicle will spawn.
- **heading**: A int, desired the heading of the vehicle.

##### Optional arguments
- **cb**: Callback that returns the vehicle the function spawned.

#### Examples

```lua tab="lua"
ESX.Game.SpawnLocalVehicle('Blista', { x = 10.0, y = 10.0, z = 10.0}, 90.0)

ESX.Game.SpawnLocalVehicle('Blista', { x = 10.0, y = 10.0, z = 10.0}, 90.0, function( vehicle )
  -- Do something with the vehicle
  print(vehicle)
end)
```

```javascript tab="javascript"
ESX.Game.SpawnLocalVehicle('Blista', { x : 10.0, y : 10.0, z : 10.0}, 90.0);

ESX.Game.SpawnLocalVehicle('Blista', { x : 10.0, y : 10.0, z : 10.0}, 90.0, function( vehicle ) {
    // Do something with the vehicle..
    console.log(vehicle);
});
```

