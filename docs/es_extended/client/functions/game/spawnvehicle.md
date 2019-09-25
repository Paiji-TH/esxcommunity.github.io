# ESX.Game.SpawnVehicle

This function spawns a vehicle.

#### Syntax

```lua
ESX.Game.SpawnVehicle(modelOrHash, coords, heading, cb)
```

##### Required arguments
- **modelOrHash**: Vehicle model or hash of the model.
- **coords**: A table that contains xyz coords where the vehicle will spawn.
- **heading**: A int, desired the heading of the vehicle.

##### Optional arguments
- **cb**: Callback that returns the vehicle the function spawned.

#### Examples

```lua tab="lua"
ESX.Game.SpawnVehicle('Blista', { x = 10.0, y = 10.0, z = 10.0}, 90.0)

ESX.Game.SpawnVehicle('Blista', { x = 10.0, y = 10.0, z = 10.0}, 90.0, function( vehicle )
  -- Do something with the vehicle
  print(vehicle)
end)
```

```javascript tab="javascript"
ESX.Game.SpawnVehicle('Blista', { x : 10.0, y : 10.0, z : 10.0}, 90.0);

ESX.Game.SpawnVehicle('Blista', { x : 10.0, y : 10.0, z : 10.0}, 90.0, function( vehicle ) {
    // Do something with the vehicle..
    console.log(vehicle);
});
```


