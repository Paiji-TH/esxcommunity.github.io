# esx:showHelpNotification

This event shows a help notification with the parsed message. These help notification support displaying button inputs, see [this list](https://pastebin.com/HPg8pYwi)

#### Syntax

```lua
TriggerClientEvent('esx:showHelpNotification', source, text)
```

##### Required arguments
- **text**: A string 


#### Examples

##### Lua
```lua
ESX.ShowNotification('Press ~INPUT_CONTEXT~')
```
