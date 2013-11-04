simpParallax
============

Simple Parallax jQuery plugin. Check out the demo in the example folder: ```example/parallax.html```

##How to use it
There are two ways to use simpParallax:
- targeting specific elements 
- using data attributes

##Requirements

jQuery and one of the simpParallax files (preferrably the minified version) must be included. Example:

```
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
<script src="../jquery.simpParallax.min.js"></script>
```

###Targeting specific elements
Simply select the element, followed by the simpParallax method.

```
$(function() {
	...

	$("#my_element").simpParallax();

	...
});
```

You will often want to pass optional parameters to control the parallax effect better. The options are:

- ```factor```: controls the speed. The higher the number, the faster the element will move up. *the default value is 0.5*

- ```parallaxtype```: can be ```top``` or ```background```defines whether the element will move up or only it's background image. *the default value is 'top'*

Example:

```
$(function() {
	...

	$("#my_element").simpParallax({
		factor: 0.4,
		parallaxtype: background
	});

	...
});
```

###Using data attributes
You may also use data attributes in your HTML element and a single call to the plugin in JavaScript. Example:

```html
<div id="my-element" data-parallax="true"></div>
```

```javascript
$(function() {
	...

	$.simpParallax();

	...
});
```

You may also need to specify options. Those can also be done through data attributes, as shown in the example below:

```html
<div id="my-element" data-parallax="true" data-factor="0.6" data-parallaxtype="top"></div>
```

```javascript
$(function() {
	...

	$.simpParallax();

	...
});
```