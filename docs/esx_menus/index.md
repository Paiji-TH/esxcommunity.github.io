# ESX menus


#### Links
- [esx_menu_default](https://github.com/ESX-Org/esx_menu_default)
- [esx_menu_list](https://github.com/ESX-Org/esx_menu_list)
- [esx_menu_dialog](https://github.com/ESX-Org/esx_menu_dialog)

#### Requirements
- [es_extended](https://github.com/ESX-Org/es_extended)

#### Downloads

```lua tab="git"
cd resources
git clone https://github.com/ESX-Org/esx_menu_default [esx]/esx_menu_default
git clone https://github.com/ESX-Org/esx_menu_list [esx]/esx_menu_list
git clone https://github.com/ESX-Org/esx_menu_dialog [esx]/esx_menu_dialog
```

```lua tab="fvm"
fvm install --save --folder=esx esx-org/esx_menu_default
fvm install --save --folder=esx esx-org/esx_menu_list
fvm install --save --folder=esx esx-org/esx_menu_dialog
```

```lua tab="manually"
Download https://github.com/ESX-Org/esx_menu_default/archive/master.zip
Download https://github.com/ESX-Org/esx_menu_list/archive/master.zip
Download https://github.com/ESX-Org/esx_menu_dialog/archive/master.zip

Put it in the resource/[esx] directory
```

#### Server.cfg
- Add these lines to your `server.cfg`. Remember do start them *after* es_extended is started, please see the start order [here](../faq/startorder.md).

```
start esx_menu_default
start esx_menu_list
start esx_menu_dialog
```