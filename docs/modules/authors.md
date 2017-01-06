<html lang="en">
<head>
	<meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta http-equiv="x-ua-compatible" content="ie=edge">

	<title>GamePlate - Home</title>
	<link rel="stylesheet" type="text/css" href="/files/css/bootstrap.4.0.0.min.css">
	<link rel="stylesheet" type="text/css" href="/files/css/bootstrap.4.0.0.docs.css">

	<link rel="stylesheet" type="text/css" href="/files/css/main.css">
	<link rel="stylesheet" type="text/css" href="/files/css/highlight/atom-one-light.css">
</head>
<body>
	<?php
	include $_SERVER["DOCUMENT_ROOT"]."/navbar.php";
	?>
	<div class="container-fluid">
		<h1>&lt;authors&gt;</h1>
		<p>Information regarding the <code>&lt;authors&gt;</code> tag and all sub-tags.</p>
		<div id="authors" class="bd-callout bd-callout-primary">
			<h4>&lt;authors&gt;</h4>
			<p>Defines the main authors of the map. Each author is listed inside an <code>&lt;author&gt;</code> tag with their respective UUIDs.</p>
		</div>
		<div id="author" class="bd-callout bd-callout-primary">
			<h4>&lt;author&gt;</h4>
			<p>Defines an author of the map.</p>
			<h4>Attributes</h4>
			<div id="author-att-uuid" class="bd-callout bd-callout-warning">
				<h4>uuid</h4>
				<p>type: <code>string</code>. Sets a map author UUID</p>
				<span class="hljs-tag">&lt;<span class="hljs-name">author</span> <span class="hljs-attr">uuid</span>=<span class="hljs-string">"db3e4ab9-7c34-4342-8aca-63db60ec8d1b"</span>/&gt;</span>
			</div>
		</div>
	</div>
	<script src="/files/js/jquery.3.1.1.min.js"></script>
	<script src="/files/js/tether.min.js"></script>
	<script src="/files/js/bootstrap.4.0.0.min.js"></script>
	<script src="/files/js/highlight.pack.js"></script>
	<script src="/files/js/main.js"></script>
</body>
</html>
