# esx_menu_default

#### Arguments
- **head**: Title of the menu
- **rows**: Table of [rows](#rows)

#### Examples

```lua tab="Basic list"
ESX.UI.Menu.Open('list', GetCurrentResourceName(), 'menu_name', {
	head = {'Column 1', 'Column 2', 'Column 3'},
	rows = {
		{
			data = 'row1',
			cols = {
				'name1',
				'name2',
				'{{' .. 'A button' .. '|button1}} {{' .. 'Another button' .. '|button2}}'
			}
		},
		{
			data = 'row2',
			cols = {
				'name1',
				'name2',
				'{{' .. 'A button' .. '|button1}} {{' .. 'Another button' .. '|button2}}'
			}
		}
	}
}, function( data, menu )
	if data.value == 'button1' then
		print('You pressed button 1')
	elseif data.value == 'button2' then
		print('You pressed button 2')
	end
end, function( data, menu )
	menu.close()
end)
```

```lua tab="Get clicked columns"
ESX.UI.Menu.Open('list', GetCurrentResourceName(), 'menu_name', {
	head = {'Column 1', 'Column 2', 'Column 3'},
	rows = {
		{
			data = 'row1',
			cols = {
				'name1',
				'name2',
				'{{' .. 'A button' .. '|button1}}'
			}
		}
	}
}, function( data, menu )
	if data.value == 'button1' then
		for i=1, #menu.data.rows do
			if data.data == menu.data.rows[i].data then
				for j=1, #menu.data.rows[i].cols do
					if not string.match(menu.data.rows[i].cols[j], '{{') then
						print(string.format('%s %s %s %s', 'Found column:', menu.data.rows[i].cols[j], 'on row: ', data.data))
					end
				end
			end
		end
	end
end, function( data, menu )
	menu.close()
end)
```

#### Rows
```lua
{
	data = 'data1',
	cols = {
		'namn1',
		'namn2',
		'{{' .. 'A button' .. '|button1}} {{' .. 'Another button' .. '|button2}}'
	}
}
```