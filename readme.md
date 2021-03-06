# Super Simple Color Picker

_Updated by: Todd Resudek http://supersimple.org_

_Branched from: Copyright 2011 Cory LaViska for A Beautiful Site, LLC. (http://abeautifulsite.net/)_

_Dual licensed under the MIT / GPLv2 licenses_


## Demo

http://supersimple.org/color-picker


## Usage

1. Link to jQuery: `<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>`
2. Link to miniColors: `<script type="text/javascript" src="jquery.miniColors.js"></script>`
3. Include miniColors stylesheet: `<link type="text/css" rel="stylesheet" href="jquery.miniColors.css" />`
4. Apply $([selector]).miniColors() to one or more INPUT elements


## Options

* __disabled__ _[true,false]_ - Disables the control on init
* __readonly__ _[true,false]_ - Makes the control read-only on init
* __predefined-colors__ _[array]_ - Makes thumbnails in selector window for colors you preset

## Specify options on creation:
    
	var predefinedColors = new Array('#eeeeee','#5fd2e6','#7daf3c','#f0910a','#be1414','#8c1ed2','#325fc8','#6a360e','#d7d746','#222222','#f1919f');
    $([selector]).miniColors(predefinedColors);
	
	or
	
	$([selector]).miniColors({
		optionName: value,
		optionName: value,
		...
	});


## Methods

Methods are called using this syntax:

	$([selector]).miniColors('methodName', [value]);

### Available Methods

* __letterCase__ _[uppercase|lowercase|null]_ - forces the hex value into upper or lowercase
* __disabled__ _[true|false]_ - sets the disabled status
* __readonly__ _[true|false]_ - sets the readonly status
* __value__ _(none)_ - gets the current value; guaranteed to return a valid hex color
* __value__ _[hex value]_ - sets the control's value
* __destroy__ _(none)_


## Events

* __change__*(hex, rgb)* - called when the color value changes; 'this' refers to the original input element
	
### Example

	$([selector]).miniColors({
		change: function(hex, rgb) { ... }
	});


## Attribution

* The color picker icon is based on an icon from the amazing Fugue icon set: http://p.yusukekamiyamane.com/
* The gradient image, the hue image, and the math functions are courtesy of the eyecon.co jQuery color picker: http://www.eyecon.ro/colorpicker/