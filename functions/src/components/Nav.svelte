<script>
	export let segment;
</script>

<style>
	nav {
		top: 0;
		background-color: #333;
		font-weight: 300;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		display: block;
		bottom: 0;
		background-color: #fff;
		border-bottom: 1px solid #333;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
		color: #fff;
	}
</style>

<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About</a></li>
		<li><a rel=prefetch aria-current="{segment === 'gallery' ? 'page' : undefined}" href="gallery">Gallery</a></li>
		<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact">Contact</a></li>
	</ul>
</nav>
