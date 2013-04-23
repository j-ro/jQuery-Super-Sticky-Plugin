#jQuery Super Sticky Plugin#
*version 1.0, April 23, 2013*

*by Jason Rosenbaum, Corporate Action Network, https://github.com/j-ro/*

A smooth sticky plugin that keeps an element stuck onscreen no matter how far the user scrolls. Handles edge cases well (like elements that are longer than browser windows, or elements or wrappers that change height after load).


##Usage##

###Setup:###

Include the jquery.superSticky.js (or jquery.superSticky.min.js) file in your HTML file after your jQuery include:

```html
<script src="jquery.superSticky.js" type="text/javascript"></script>
```

Then call the plugin on a DOM element you want to make sticky using something like the examples below.

The plugin should work on sidebars in a wide range of DOM setups -- let me know if you have issues with your implementation in the issues section!


###Options:###
 		
**wrapper** -- a jQuery selector identifying the element that wraps around the sticky sidebar *(default: the sticky element's parent)*
 		
**padding_top** -- the amount of padding you want the sticky sidebar to maintain from the top of the browser window, in pixels. If this is larger than the element's initial top offset, top padding will be set to the elements initial top offset instead. *(default: 0)*
 		
**padding_bottom** -- the amount of padding you want the sticky sidebar to maintain from the bottom of the wrapper element, in pixels *(default: 0)*


###Methods:###

**init** -- called on load and when either the element or its wrapper change height


###Examples:###

```javascript		
$(document).ready(function() {
	//use defaults
	$('.sticky_element').superSticky();
});
```
 
```javascript		
$(document).ready(function() {
	//use custom options
	$('.sticky_element').superSticky({
		padding_top : 120,
		padding_bottom : 50,
		wrapper: '.action_page'
	});
});
```
 
##License	

Includes the jQuery Mutate plugin: https://github.com/jqui-dot-net/jQuery-mutate	
 		
Other code copyright (c) 2013 Jason Rosenbaum

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.