jQueryUI Limitslider
====================
Version v1.1.1

Copyright &copy; 2011-2015 Martijn van der Lee (http://martijn.vanderlee.com).
MIT Open Source license applies.

A slider allowing multiple sliders and ranges with all sorts of optional
limitations in position/size/distance. Also includes optional labels on the
sliders and hover titles.

Uses jQueryUI's slider as basis, so both small and reliable.

Features
--------
-	Multiple sliders.
-	Multiple ranges.
-	Allows or blocks crossing of sliders.
-	Minimum distance between sliders.
-	Minimum/maximum position for all or individual sliders.
-	Label on the sliders.
-	Titles on sliders.
-	Use all of jQueryUI's slider functionality.

Everything is optional. If you want, you can use the limitslider plugin like a
plain slider.

Download
--------
jQuery v1.3.0 or higher required.

jQueryUI v1.8.0 or higher required.

Current version: https://github.com/vanderlee/limitslider/archive/master.zip

Sourcecode on Github: https://github.com/vanderlee/limitslider

Quick start
-----------
Here's a short code fragment, demonstrating how to use limitslider.

There are many more options to tailor it to your needs.

	<div class="example-basic"></div>

	<script>
		$(function() {
			$('.example-basic').limitslider();
		});
	</script>

Future
------
-	Ticks
-	Init event
-	Vertical ranges
-	Title/label callback; index of slider, before/after ranges, options, etc.?
-	Easy access to lengths or ranges in events
-	Visual styling (i.e. height)

Documentation
=============
'.limitslider(options)'
-----------------------
Create one or more limitsliders or access an existing limitslider.

Limitslider is based on the standard jQueryUI Slider widget and inherits it's
API interface.

This means all options, methods and events describer for it are
supported in addition to all the options, methods and events described below.

API documentation for jQueryUI Slider can be found here:
http://api.jqueryui.com/slider/

### Options

-	**classEven** (string, default: `ui-slider-handle-even`)

>	Name of a class that is set for every even (second, fourth, etc.) slider
	handle.

-	**classOdd** (string, default: `ui-slider-handle-odd`)

>	Name of a class that is set for every odd (first, third, etc.) slider
	handle.

-	**gap** (positive float, default: `undefined`)

>	Sets the minimal distance between individual sliders. If set to `undefined`,
	sliders may cross each other. Set to `0`, they may touch, but not cross.
	Any greater value will force the sliders to be atleast the specified amount
	apart.

>	Units are in parts of the slider range defined by `min` and `max`.

-	**label** (boolean or function, default: `false`)

>	If enabled, each slider will have a label printed on it.

>	By default, the	label will simply contain the current position number.

>	Alternatively, you can set a function which will receive the current
	position as it's first (and only) argument. The function should return a
	string. Please keep in mind that space on the slider buttons is limited.

-	**limit** (default: `undefined`)

>	Sets the lower and upper limit (or gap) of all sliders.

-	**limits** (default: `undefined`)

>	@TODO

-	**max** (positive float, default: `100`)

>	The maximum value of the range.

-	**min** (positive float, default: `0`)

>	The minimum value of the range.

-	**ranges** (default: `undefined`)

>	@TODO

-	**title** (boolean or function, default: `false`)

>	If enabled, each slider will have a title shown by hovering over it.

>	By default, the title will simply contain the current position number.

>	Alternatively, you can set a function which will receive the current
	position as it's first (and only) argument. The function should return a
	string.

-	**values** (default: `[]`)

>	Array or values for the positions of the sliders. The number of items in
	the array determines the number of sliders. If not specified, the plugin
	will default to a single slider as per jQueryUI's slider.

### Methods

-	**destroy**  (inherited from jQueryUI slider)

-	**disable**  (inherited from jQueryUI slider)

-	**enable**  (inherited from jQueryUI slider)

-	**instance**  (inherited from jQueryUI slider)

-	**option**  (inherited from jQueryUI slider)

>	Also supports all the additional options for the limitslider widget.

-	**value**  (inherited from jQueryUI slider)

-	**values** (inherited from jQueryUI slider)

>	Get the value for all handles.

>	Code example `var values = $(".selector").slider("values");`

-	**widget** (inherited from jQueryUI slider)

### Events

-	**change** (inherited from jQueryUI slider)

-	**create** (inherited from jQueryUI slider)

-	**slide** (inherited from jQueryUI slider)

-	**start** (inherited from jQueryUI slider)

-	**stop** (inherited from jQueryUI slider)