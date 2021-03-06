---
layout: post
title:  "DRAGGING MULTIPLE ELEMENTS"
date:   2014-01-17 18:58:00
categories: posts
---

<style type="text/css">
	.jsplumb-drag-selected {
		border: 1px solid orange;
		background-color: gold;
	}
	
	#demo {
		height:400px;
	}

	.clearSelection {
		position:absolute;
		right:10px;
		top:5px;
		letter-spacing:3px;
	}
</style>

A new feature that is available in jsPlumb 1.6.0 is the ability to drag multiple elements. This is made possible by the fact that there is now a version of jsPlumb ("Vanilla" jsPlumb) that does not have a dependency on jQuery, MooTools or YUI (as all previous versions have done); instead, to support dragging, it depends on a new project - [Katavorio](https://github.com/jsplumb/katavorio) - which was written specifically to provide two features that are missing in other drag libraries:

- dragging multiple elements
- supporting multiple drag/drop scopes

both of these issues have been raised in both the jsPlumb forums and in the issue tracker many times.

Katavorio does not, of course, depend on jsPlumb, and can be used elsewhere.  A discussion of how to do so is outside the scope of this post - if you're interested, check out the code, and if you have any questions, <a href="mailto:simon@jsplumbtoolkit.com">drop me a line</a>. At some stage I will get around to documenting its functionality properly.

### Drag Selection

The basic new concept introduced into jsPlumb is that of the _drag selection_ - a list of elements that, whenever some element is dragged, should also be dragged, and whose location relative to the element being dragged should remain constant. To support this, there are three new methods available on an instance of jsPlumb:

- `addToDragSelection`

Takes as argument either a String, representing a selector (which is to say that to specify a single element using a string you must prepend the id with a #), an Element, a NodeList, an array of Elements, or a list of Strings (representing a list of selectors).  Adds all of the found elements to the current drag selection.

- `removeFromDragSelection`

Takes as argument either a String, representing a selector (which is to say that to specify a single element using a string you must prepend the id with a #), an Element, a NodeList, an array of Elements, or a list of Strings (representing a list of selectors).  Removes all of the found elements from the current drag selection.

- `clearDragSelection`

Clears the current drag selection.

### Example

In this example we have a bunch of elements that each have a `+` and a `-` button, to add or remove the element to/from the drag selection. 

Each element is configured to be a connection source (you can drag new connections from the blue div; the rest of the 
element acts as a drag handle for the entire element) and target, using Continuous anchors.

<div class="demo" id="demo">
	<div class="clearSelection"><a href="#">clear drag selection</a></div>
	<div id="w1" class="w" style="left:25px;top:35px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
	<div id="w2" class="w" style="left:185px;top:55px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
    <div id="w3" class="w" style="left:145px;top:175px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
    <div id="w4" class="w" style="left:425px;top:115px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
    <div id="w5" class="w" style="left:465px;top:345px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
    <div id="w6" class="w" style="left:305px;top:115px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
    <div id="w7" class="w" style="left:5px;top:235px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
    <div id="w8" class="w" style="left:325px;top:3px"><a class="add">+</a><a class="remove">-</a><div class="foo" style="height:10px;width:10px;background-color:blue"></div></div>
</div>

### CSS

You will most likely have noticed in the example that whenever you add an element to the drag selection its appearance changes.  This is achieved via CSS: jsPlumb adds a class to each element that is part of the drag selection:

`jsplumb-drag-selected`


{% include dom.jsplumb.html %}
<script src="/assets/multiple-drag.js"></script>


