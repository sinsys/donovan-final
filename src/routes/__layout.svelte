<script lang="ts">
	import Header from '$lib/header/Header.svelte'
	import '../app.css'
	const tradeMarkSymbol = '\u2122'
	const title = 'Donovan Wedington'
	const currentYear = new Date().getFullYear()
	const developer = 'Nico Web Development'
	const footerText = `${tradeMarkSymbol} ${title} - ${currentYear} - ${developer}`
</script>

<Header />

<main>
	<slot />
</main>

<footer>
	<p>{footerText}</p>
</footer>

<style lang="scss">
	
	main {
		display: flex;
		flex-grow: 1;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		min-height: 10vh;
		box-sizing: border-box;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
