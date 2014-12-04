# angular-natural-language

## About
Natural language form element directives for AngularJS.

Forked from [Venturocket/angular-natural-language](https://github.com/Venturocket/angular-natural-language).

## Usage

### nlSelect
#### Markup
As an element:
```
<nl-select
	value="{string}"
	options="{string}"
	multiple="{string}"
	empty="{string}"
	change="{function}"
	required>
</nl-select>
```
As an attribute:
```
<div
	nl-select
	value="{string}"
	options="{string}"
	multiple="{string}"
	empty="{string}"
	change="{function}"
	required>
</div>
```

#### Parameters
|Param		|Type	|Details|
|-----------|-------|-------|
|value		|string	|Assignable angular expression to data-bind to. (think of it like ng-model)|
|options	|string	|Expression to data-bind to. (the options list section below shows the accepted formats)|
|multiple	|string (optional) |Simulates the multiple attribute on a normal select. The string value given is used as the conjunction between selections. Defaults: "and"|
|all        |string (optional)  |Only applicable if multiple is enabled. Text to display for the select all option.|
|none       |string (optional)  |Only applicable if multiple is enabled. Text to display for the select none option.|
|empty		|string (optional) |What to display when no options are selected. Default: "none" (this is only used if multiple is specified)|
|change		|function |Function that gets called when the value of the select changes|
|required	|boolean|Simulates the required attribute on a normal select|

#### Options List
The options list can be in one of the 4 following formats:

Array of labels/values:
```
['one', 'two', 'three', ...]
```
Array of objects:
```
[
	{ label: 'one', value: 'ten' },
	{ label: 'two', value: 'nine' },
	{ label: 'three', value: 'eight' },
	...
]
```
Object of labels/values:
```
{ 'one':'ten', 'two':'nine', 'three':'eight', ... }
```
Object of objects:
```
{
	'one':{ label: 'one', value: 'ten' },
	'two':{ label: 'two', value: 'nine' },
	'three':{ label: 'three', value: 'eight' },
	...
}
```
--
### nlText
#### Markup
As an element:
```
<nl-text
	value="{string}"
	placeholder="{string}"
	subline="{string}"
	name="{string}"
	change="{function}"
	html5type="{string}"
	required>
</nl-text>
```
As an attribute:
```
<div
	nl-text
	value="{string}"
	placeholder="{string}"
	subline="{string}"
	name="{string}"
	change="{function}"
	html5type="{string}"
	required>
</div>
```

#### Parameters
|Param		|Type	|Details|
|-----------|-------|-------|
|value		|string	|Assignable angular expression to data-bind to. (think of it like ng-model)|
|placeholder|string (optional) |String to use as the placeholder for the input and default text for the view|
|subline	|string (optional) |Small bit of directions to display just below the input|
|name		|string (optional) |Passed directly to the actual input element|
|change		|function |Function that gets called when the value of the input changes|
|html5type	|string |html5 input type|
|required	|boolean|Simulates the required attribute on a normal text input|
