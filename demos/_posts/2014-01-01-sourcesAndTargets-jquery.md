---
layout: demo
library: "jquery"
libraryName: "jQuery"
demo: "sourcesAndTargets"
categories: [demos]
permalink: "demo/sourcesAndTargets/jquery.html"
---

<div class="explanation">
	<h4>SOURCES &amp; TARGETS</h4>                    
	<p>Drag Connections from the blue element to any of the green ones. You can also drag existing
		Connections from one green element to another - Connections are, by default, detachable (this behaviour can be overridden).</p>
	<p>The <strong>makeSource</strong> and <strong>makeTarget</strong>functions provide an alternative means of setting up your UI to support draggable connections - here we treat entire
	elements as sources and targets, and only when Connections are established do we assign Endpoints for them.</p>
	<p>The blue element is configured as a Connection source (and is not draggable), with a list of possible Anchor locations.</p>          
	<p>
	The `disable` link is excluded from being a drag source through the use of the `filter` parameter on the makeSource call.
	</p>
	<p>The green elements are configured as Connection targets, with a `Top` anchor, and are draggable</p>
</div>                  
<div class="demo source-target-demo" id="source-target-demo">
	<div class="window" id="sourceWindow1">           
		<strong>Window 1</strong>
		<a href="#" id="enableDisableSource">disable</a>                
	</div>
	<div class="window smallWindow" id="targetWindow2"><strong>Window 2</strong><br/><br/></div>
	<div class="window smallWindow" id="targetWindow3"><strong>Window 3</strong><br/><br/></div>
	<div class="window smallWindow" id="targetWindow4"><strong>Window 4</strong><br/><br/></div>
	<div class="window smallWindow" id="targetWindow5"><strong>Window 5</strong><br/><br/></div>
	<div class="window smallWindow" id="targetWindow6"><strong>Window 6</strong><br/><br/></div>
</div>