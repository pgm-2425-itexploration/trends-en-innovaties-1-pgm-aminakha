<script>
	import Header from "./lib/components/partials/Header/Header.svelte";
	import Calculator from "./lib/components/Calculator/Calculator.svelte";
</script>

<section class="container">
	<Header />
<main>
	
	<h1>Hello WORLD!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<Calculator />
</main>

</section>

<style>
	.container {
		text-align: center;
		padding: 1em;
		max-width: 15rem;
		margin: 0 auto;
	}

	

	@media (min-width: 640px) {
		.container {
			max-width: none;
		}
	}
</style>