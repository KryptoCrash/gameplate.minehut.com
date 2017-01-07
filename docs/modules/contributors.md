
<div class="container-fluid">
	<h1>&lt;contributors&gt;</h1>
	<p>Information regarding the <span class="hljs-tag">&lt;<span class="hljs-name">contributors</span>&gt;</span> tag and all sub-tags.</p>
	<div id="contributors" class="bd-callout bd-callout-primary">
		<h4>&lt;contributors&gt;</h4>
		<p>Defines the main contributors of the map. Each contributor is listed inside an <code>&lt;contributor&gt;</code> tag with their respective UUIDs.
		<br>Contributors can be thought of similarly to the author(s) of the map, but did not directly author it.</p>
	</div>
	<div id="contributor" class="bd-callout bd-callout-primary">
		<h4>&lt;contributor&gt;</h4>
		<p>Defines an contributor to the map.</p>
		<h4>Attributes</h4>
		<div id="contributor-att-uuid" class="bd-callout bd-callout-warning">
			<h4>uuid</h4>
			<p>type: <code>string</code>. Sets a contributor UUID</p>
			<span class="hljs-tag">&lt;<span class="hljs-name">contributors</span>&gt;</span><br>
				<span class="hljs-tag">&lt;<span class="hljs-name">contributor</span> <span class="hljs-attr">uuid</span>=<span class="hljs-string">"2dc9b2a1-6063-499b-9685-aa97b978707a"</span>/&gt;</span><br>
			<span class="hljs-tag">&lt;/<span class="hljs-name">contributors</span>&gt;</span>
		</div>
		<div id="contributor-att-contribution" class="bd-callout bd-callout-warning">
			<h4>contribution</h4>
			<p>type: <code>string</code>. Defines what the contributor added to the map, or how they helped in its development.</p>
			<span class="hljs-tag">&lt;<span class="hljs-name">contributors</span>&gt;</span><br>
				<span class="hljs-tag">&lt;<span class="hljs-name">contributor</span> <span class="hljs-attr">contribution</span>=<span class="hljs-string">"Map Layout and XML help."</span> <span class="hljs-attr">uuid</span>=<span class="hljs-string">"2dc9b2a1-6063-499b-9685-aa97b978707a"</span>/&gt;</span><br>
			<span class="hljs-tag">&lt;/<span class="hljs-name">contributors</span>&gt;</span>
		</div>
	</div>
</div>
