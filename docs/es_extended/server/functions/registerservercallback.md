# ESX.RegisterServerCallback

This function registers a server callback.

#### Syntax

```lua
ESX.RegisterServerCallback('name', function( source, callback, data ) end)
```

##### Required arguments
- **name**: A string representing the callback name.
- **source**: The source of the player who calls the function.
- **callback**: A function that sends back the data to the [TriggerServerCallback](../../client/functions/triggerservercallback.md) function.

##### Optional arguments
- **data**: Data sent from the [TriggerServerCallback](../../client/functions/triggerservercallback.md) function.

#### Examples

##### Lua
```lua
ESX.RegisterServerCallback('name', function( source, callback, data )
    -- Do something with the optional data..
    print(data)
    
    -- Do something with the source..
    TriggerClientEvent('name', source)

    -- Send data back to the TriggerServerCallback
    callback('data')
end)
```

##### JavaScript
```javascript
ESX.RegisterServerCallback('name', function( source, callback, data ) {
    // Do something with the optional data..
    console.log(data);

    // Do something with the source..
    emitNet('name', source);

    // Send data back to the TriggerServerCallback
    callback('data');
});
```