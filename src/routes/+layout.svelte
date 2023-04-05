<script lang="ts">
	import './app.css';
	import { base } from '$app/paths';
	import Socials from '$lib/socials.svelte';
</script>

<div id="page">
	<header>
		<span id="head_footer_highlight" />
		<nav>
			<a class="default_footer_text" href="{base}/">About me</a>
			<a class="default_footer_text" href="{base}/skills">Skills</a>
			<a class="default_footer_text" href="{base}/expr">Portfolio</a>
			<a class="default_footer_text" href="{base}/joke">Jokes</a>
		</nav>
	</header>
	<main>
		<div class="main-information">
			<slot />
		</div>
	</main>
	<footer>
		<Socials />
	</footer>
</div>

<style>
	header {
		background-color: #17252a;
		box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.2);
		text-align: center;
		font-family: 'Helvetica Neue', sans-serif;
		font-size: 1.5em;
		color: #f5f5f5;
		display: grid;
		padding: 2%;
		grid-template-columns: auto 1fr auto;
		align-items: center;
	}

	#head_footer_highlight {
		font-weight: 400;
		font-size: larger;
		color: #f5f5f5;
		text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
	}

	.default_footer_text {
		text-align: right;
		font-weight: 100;
		font-size: larger;
		color: #e1ebe9;
		text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
	}

	/* Add a hover effect to the header */
	header:hover {
		background-color: #0c1c20;
	}
</style>
