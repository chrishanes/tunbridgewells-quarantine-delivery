<script>
	import Header from '../components/Header.svelte';
	import Footer from '../components/Footer.svelte';
	import { twdata } from '../store.js';

	export let data;

	twdata.set(data)
	

</script>

<script context="module">
	// const apiURL = 'https://st7ot1tu57.execute-api.us-west-2.amazonaws.com/tw-community/community-data';
	const apiURL = 'https://rz6xb697g4.execute-api.eu-west-2.amazonaws.com/production/twdelivery';

	export async function preload({ params, query }) {
		
		const res = await this.fetch(apiURL);
		const data = await res.json();

		twdata.set(data);

		return {
			data: data
		}

	}

</script>

<style>
	.container {
		margin: 0 auto;
		max-width: 1440px;
		position: relative;
	}

	.grid {
		display: grid;
		flex-wrap: nowrap;
		grid-gap: 16px;
		grid-template-columns: repeat(12, 1fr);
		margin: 10px;
	}

	@media (min-width: 768px) {
		.grid {
			margin: 10px 16px;
		}
	}

	.header-wrapper {
		padding: 10px 0 20px 0;
	}

	@media (min-width: 768px) {
		.header-wrapper {
			padding: 20px 0 30px 0;
		}
	}

	main {
		box-sizing: border-box;
	}
</style>

<div class="container">
	<div class="grid header-wrapper">
		<Header />
	</div>

	<main class="grid">
		<slot></slot>
	</main>

	<Footer />
</div>