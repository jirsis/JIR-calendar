# Module: JIR-Calendar
The `JIR-calendar` module is based in `calendar` default modules of the MagicMirror.
This module displays events from a public .ical calendar and define diferents symbols
by diferents regex.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
	{
		module: "JIR-calendar",
		position: "top_left",	// This can be any of the regions. Best results in left or right regions.
		config: {
			// The config property is optional.
			// If no config is set, an example calendar is shown.
			// See 'Configuration options' for more information.
		}
	}
]
````

## Configuration options

This module accepts all properties defined by [calendar](https://github.com/MichMich/MagicMirror/tree/master/modules/default/calendar),
and add one usefull option:


| Option                       | Description
| ---------------------------- | -----------
| `customSymbols`              | Array for objects to define the symbol-name pattern. / **Possible values:** `[{name: "birthday", symbol: "birthday-cake"}]`<br> **Default value:** `[]`


#### Default value:
````javascript
config: {
	colored: false,
	calendars: [
		{
			url: 'http://www.calendarlabs.com/templates/ical/US-Holidays.ics',
			symbol: 'calendar',
			customSymbols: [
				{name: "birthday", symbol: "birthday-cake"},
				{name: "doctor", symbol: "user-md"}
			]
		},
	],
}
````
