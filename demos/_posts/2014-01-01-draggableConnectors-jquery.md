---
layout: demo
library: "jquery"
libraryName: "jQuery"
demo: "draggableConnectors"
categories: [demos]
permalink: "demo/draggableConnectors/jquery.html"
---

<div class="explanation">         
	<h4>DRAG &amp; DROP</h4>                           
	<p>Drag from any Endpoint to similar Endpoints on other elements to create Connections.</p>
	<p>Blue Endpoints use a <strong>beforeDrop</strong> interceptor.  This enables
	you to intercept a new connection and decide whether or not you wish to allow it to proceed. They are also configured to automatically reattach if you drag a Connection off and drop it on the background.</p>
	<p>Yellow Endpoints are configured to use a <strong>beforeDetach</strong> interceptor, which provides a way to programmatically override a Connection detach. Yellow connections are painted with the Straight connector</p>            
	<p>Green Endpoints support up to three Connections. Once a green Endpoint has three connections, when you drag from it you will drag the oldest connection made on the Endpoint.</p>
	<div class="commands">
		<a id="clear" class="cmd" href="#">clear plumbing</a>
	</div>
</div>  
<div id="drag-drop-demo" class="demo drag-drop-demo">                                
	<div class="window" id="dragDropWindow1">one<br/><br/><a href="#" class="cmdLink hide" rel="dragDropWindow1">toggle connections</a><br/><a href="#" class="cmdLink drag" rel="dragDropWindow1">disable dragging</a><br/><a href="#" class="cmdLink detach" rel="dragDropWindow1">detach all</a></div>
	<div class="window" id="dragDropWindow2">two<br/><br/><a href="#" class="cmdLink hide" rel="dragDropWindow2">toggle connections</a><br/><a href="#" class="cmdLink drag" rel="dragDropWindow2">disable dragging</a><br/><a href="#" class="cmdLink detach" rel="dragDropWindow2">detach all</a></div>
	<div class="window" id="dragDropWindow3">three<br/><br/><a href="#" class="cmdLink hide" rel="dragDropWindow3">toggle connections</a><br/><a href="#" class="cmdLink drag" rel="dragDropWindow3">disable dragging</a><br/><a href="#" class="cmdLink detach" rel="dragDropWindow3">detach all</a></div>
	<div class="window" id="dragDropWindow4">four<br/><br/><a href="#" class="cmdLink hide" rel="dragDropWindow4">toggle connections</a><br/><a href="#" class="cmdLink drag" rel="dragDropWindow4">disable dragging</a><br/><a href="#" class="cmdLink detach" rel="dragDropWindow4">detach all</a></div>          
	<div id="list"></div>                
</div>