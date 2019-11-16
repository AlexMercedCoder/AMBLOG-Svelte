<script>
	import Posts from "./Posts.svelte";
</script>

<main>
	<h1>Welcome!</h1>
	<p>This is another front-end application for my Contentful headless blog. This application was created using the Svelte compiler!</p>
	<Posts/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
