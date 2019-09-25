# ESX.TriggerServerCallback

This function triggers a server callback. [ESX.RegisterServerCallback](../../server/functions/registerservercallback.md).

#### Syntax

```lua
ESX.TriggerServerCallback('name', function( callback ) end, data)
```

##### Required arguments
- **name**: A string representing the callback name to call.
- **callback**: The data sent back from the server.

##### Optional arguments
- **data**: Data sent to the server, could be any data type.

#### Examples

```lua tab="lua"
ESX.TriggerServerCallback('name', function( callback )
    -- Do something with the callback..
    print(callback)
end, 'data')
```

```javascript tab="javascript"
ESX.TriggerServerCallback('name', function( callback ) {
    // Do something with the callback..
    console.log(callback);
}, 'data');
```