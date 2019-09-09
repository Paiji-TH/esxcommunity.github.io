# ESX.ShowAdvancedNotification

This function shows an advanced notification.

#### Syntax

```lua
ESX.ShowAdvancedNotification(title, subject, text, icon, iconType)
```
##### Required arguments
- **title**: A string 
- **subject**: A string 
- **text**: A string 
- **icon**: A string, see [Icons](#icons)
- **iconType**: A int, see [Icon Types](#icons-types) 

#### Examples

##### Lua
```lua
ESX.ShowAdvancedNotification('title', 'subject', 'text', 'CHAR_AMMUNATION', 1)
```

##### Result

![Advanced Notification Example Picture](https://i.imgur.com/bX1oxrF.jpg)

#### Icons

To specify an icon you can either simply parse an already existing notification image, or you can create a player mugshot with ESX.

* [Existing Image](https://wiki.gtanet.work/index.php?title=Notification_Pictures)
* [Player Mugshots](game/getpedmugshot.md)

#### Icon Types

* `1` --> Chat Box
* `2` --> Email
* `3` --> Add Friend Request
* `7` --> Right Jumping Arrow
* `8` --> RP Icon
* `9` --> $ Icon
