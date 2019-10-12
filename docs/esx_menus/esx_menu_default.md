# esx_menu_default

#### Arguments
- **title**: Title of the menu
- **align**: [Location](#align) of the menu
- **elements**: Menu [elements](#elements)

#### Examples

```lua tab="Basic menu"
ESX.UI.Menu.Open('default', GetCurrentResourceName(), 'menu_name', {
	title    = 'A title',
	elements = {
        {label = 'A label', value = 'avalue'},
        {label = 'A label 1', value = 'avalue1'},
	}
}, function( data, menu )
	if data.current.value == 'avalue' then
        print('Do something..')
    elseif data.current.value == 'avalue1' then
        print('Do something..')
	end
end, function( data, menu )
	menu.close()
end)
```

```lua tab="Nested menus"
ESX.UI.Menu.Open('default', GetCurrentResourceName(), 'menu_name', {
	title    = 'A title',
	elements = {
		{label = 'A label', value = 'avalue'},
	}
}, function( data, menu )
	if data.current.value == 'avalue' then
		ESX.UI.Menu.Open('default', GetCurrentResourceName(), 'menu_name2', {
			title    = 'A title 2',
			elements = {
				{label = 'A label 2', value = 'avalue'},
			}
		}, function( data2, menu2 )
			if data2.current.value == 'avalue' then
				print('Do something..')
			end
		end, function( data2, menu2 )
			menu2.close()
		end)
	end
end, function( data, menu )
	menu.close()
end)
```

```lua tab="Slider menu"
ESX.UI.Menu.Open('default', GetCurrentResourceName(), 'menu_name', {
	title    = 'A title',
	elements = {
		{label = 'Just a label', value = 'avalue'},
		{
			label   = 'A slider label',
			name    = 'A name',
			value	= 0,
			min		= 0,
			max 	= 100,
			type    = 'slider'
		}
	}
}, function( data, menu )
	print(string.format('%s %s', 'Selected element: ', json.encode(data.elements[1])))
	print(string.format('%s %s', 'Selected value: ', json.encode(data.elements[1].value)))
end, function( data, menu )
	menu.close()
end)
```

#### Align
left, top-left, top, top-right, right, bottom-right, bottom, bottom-left, center

#### Elements
```lua
elements = {
    -- Regular label with a value
    {label = 'A label', value = 'avalue'},
    -- Slider
    {label = 'A label', name = 'A name', value = 0, min = 0, max = 100, type = 'slider'}
}
```