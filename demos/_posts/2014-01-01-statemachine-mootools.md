---
layout: demo
library: "mootools"
libraryName: "MooTools"
demo: "statemachine"
categories: [demos]
permalink: "demo/statemachine/mootools.html"
---

<div class="explanation">
	<h4>STATE MACHINE</h4>
	<p>Nodes are connected with the StateMachine connector.</p>
	<p>Endpoints are located with 'Continuous' anchors, which are anchors whose location is calculated based on the location of all other connected elements, and which guarantee a unique endpoint per connection.
	</p>                                
	<p>Click and drag new Connections from the orange div in each element; the main elements in the UI are configured to be Connection targets. You can drag from one of these divs onto its parent element to create a 'loopback' connection. Each element supports up to 5 Connections.</p>
	<p>Click on a Connection to delete it.</p>
</div>  
<div class="demo statemachine-demo" id="statemachine-demo">
	<div class="w" id="opened">BEGIN<div class="ep"></div></div>
	<div class="w" id="phone1">PHONE INTERVIEW 1<div class="ep"></div></div>
	<div class="w" id="phone2">PHONE INTERVIEW 2<div class="ep"></div></div>
	<div class="w" id="inperson">IN PERSON<div class="ep"></div></div>
	<div class="w" id="rejected">REJECTED<div class="ep"></div></div>                           
</div>
