# esx:playerLoaded

Player has loaded in, called from the server event es:playerLoaded.

#### Syntax

```lua
AddEventHandler('esx:playerLoaded', function( xPlayer ) end)
```

##### Optional arguments
- **xPlayer**: The xPlayer, only necessary if you want to do something with the player.

#### Examples

##### Lua
```lua
AddEventHandler('esx:playerLoaded', function( xPlayer ) 
    print('Player has loaded in')
end)
```

##### JavaScript
```javascript
onNet('esx:playerLoaded', function( xPlayer ) {
    console.log('Played has loaded in');
});
```