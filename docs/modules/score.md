<div class="container-fluid">
	<h1>&lt;score&gt;</h1>
	<p>Information regarding the <span class="hljs-tag">&lt;<span class="hljs-name">score</span>&gt;</span> tag and all sub-tags.</p>
	<div id="score" class="bd-callout bd-callout-primary">
		<h4>&lt;score&gt;</h4>
		<p>Defines the main scoreboard objective of the map.</p>
	</div>
	<div id="limit" class="bd-callout bd-callout-primary">
		<h4>&lt;limit&gt;</h4>
		<p>Sets the limit of the scoreboard. Values cannot go past the one set here.</p>
		<span class="hljs-tag">&lt;<span class="hljs-name">limit</span>&gt;</span>10<span class="hljs-tag">&lt;/<span class="hljs-name">limit</span>&gt;</span>
	</div>
	<div id="event" class="bd-callout bd-callout-primary">
		<h4>&lt;%event%&gt;</h4>
		<p>There are several events that can be used to effect the value of the score.<br>
		<span class="tag tag-danger">NOTE</span><br>
		The tag itself is NOT named <code><%event%></code>. This is a shorthand for these docs. The event names are listed here.</p>
		<h4>Event Names</h4>
		<div id="event-kill" class="bd-callout bd-callout-success">
			<h4>&lt;kill&gt;</h4>
			<p>Event is called when a player is killed. Score value changes based on the set value.</p>
			<span class="hljs-tag">&lt;<span class="hljs-name">score</span>&gt;</span><br>
				 <span class="hljs-comment">&lt;!-- Increases the score by 2 --&gt;</span><br>
				<span class="hljs-tag">&lt;<span class="hljs-name">kill</span>&gt;</span>2<span class="hljs-tag">&lt;/<span class="hljs-name">kill</span>&gt;</span><br>
			<span class="hljs-tag">&lt;/<span class="hljs-name">score</span>&gt;</span>
		</div>
	</div>
	<div id="goal" class="bd-callout bd-callout-primary">
		<h4>&lt;goal&gt;</h4>
		<p>A goal line for the score value. Event is run when the specified team reaches the specified value<br>
		<h4>Attributes</h4>
		<div id="goal-att-team" class="bd-callout bd-callout-warning">
			<h4>team</h4>
			<p>The team the goal is set for</p>
			<span class="hljs-tag">&lt;<span class="hljs-name">goal</span> <span class="hljs-attr">team</span>=<span class="hljs-string">"red"</span>/&gt;</span>
		</div>
		<div id="goal-att-amount" class="bd-callout bd-callout-warning">
			<h4>amount</h4>
			<p>The value needed for the goal to be met</p>
			<span class="hljs-tag">&lt;<span class="hljs-name">goal</span> <span class="hljs-attr">amount</span>=<span class="hljs-string">"3"</span>/&gt;</span>
		</div>
	</div>
</div>