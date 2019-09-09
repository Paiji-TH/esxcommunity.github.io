# ES_Extended
Short for EssentialMode_Extended. The core resource of the ESX framework.

ES_Extended is a roleplay framework for FiveM. It is developed on top of [EssentialMode](https://forum.fivem.net/t/release-essentialmode-base/3665).

#### Links
- [ESX Official Documentation](https://esx-org.github.io/)
- [ESX Community Documentation](https://esx-community.github.io/)
- [ES Documentation](https://wiki.kanersps.pw/display/FIV/Documentation)
- [FiveM Forum Thread](https://forum.fivem.net/t/release-esx-base/39881)
- [FiveM Native Reference](https://runtime.fivem.net/doc/reference.html)

#### Features
- Accounts (bank / black money). You can add further accounts
- Advanced inventory system (press `F2` ingame)
- Job system
- Loadouts and position synced in database
- The best framework out there for RP servers
- i18n (locale) system
- Plenty of plugins available

#### Requirements
This order also applies in the startup order.

- [mysql-async](https://github.com/brouznouf/fivem-mysql-async)
- [essentialmode](https://github.com/kanersps/essentialmode)
- [esplugin_mysql](https://github.com/kanersps/esplugin_mysql)
- [async](https://github.com/ESX-Org/async)

#### Download

##### Using [fvm](https://github.com/qlaffont/fvm-installer)
```
fvm install --save --folder=essential esx-org/es_extended
fvm install --save --folder=esx esx-org/esx_menu_default
fvm install --save --folder=esx esx-org/esx_menu_dialog
fvm install --save --folder=esx esx-org/esx_menu_list
```

##### Using Git

```
cd resources
git clone https://github.com/ESX-Org/es_extended [essential]/es_extended
git clone https://github.com/ESX-Org/esx_menu_default [esx]/[ui]/esx_menu_default
git clone https://github.com/ESX-Org/esx_menu_dialog [esx]/[ui]/esx_menu_dialog
git clone https://github.com/ESX-Org/esx_menu_list [esx]/[ui]/esx_menu_list
```

##### Manually
- Download https://github.com/ESX-Org/es_extended/releases/latest
- Put it in the `resource/[essential]` directory
- Download https://github.com/ESX-Org/esx_menu_default/releases/latest
- Put it in the `resource/[esx]/[ui]` directory
- Download https://github.com/ESX-Org/esx_menu_dialog/releases/latest
- Put it in the `resource/[esx]/[ui]` directory
- Download https://github.com/ESX-Org/esx_menu_list/releases/latest
- Put it in the `resource/[esx]/[ui]` directory

#### Installation
- Import `es_extended.sql` in your database
- Configure your `server.cfg` to look like this

```
start mysql-async
start essentialmode
start esplugin_mysql

start es_extended

start esx_menu_default
start esx_menu_list
start esx_menu_dialog
```
Copied from [github.com/ESX-Org/es_extended](https://github.com/ESX-Org/es_extended/blob/master/README.md).