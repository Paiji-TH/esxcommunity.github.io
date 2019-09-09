# ESX.SetPlayerData

This function sets player data.

#### Syntax

```lua
ESX.SetPlayerData(key, val)
```

##### Required arguments
- **key**: A string that represents the index of the table, see [keys](#keys).
- **val**: Could be any data type depending on the [key](#keys).

#### Examples

##### Lua
```lua
ESX.SetPlayerData('identifier', 'steam:123')
ESX.SetPlayerData('money', 1)
ESX.SetPlayerData('accounts', {})
```

#### Keys
string **identifier** - Steam identifier <br/>
int **money** - Players cash <br/>
table **accounts** - Players bank and black_money <br/>
table **inventory** - Players inventory <br/>
table **loadout** - Players loadout <br/>
table **job** - Players current job <br/>
table **lastPosition** - Players latest coordinates
