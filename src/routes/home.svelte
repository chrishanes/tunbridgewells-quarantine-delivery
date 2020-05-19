<script>
	import Content from '../components/Content.svelte';
	// import { onMount } from 'svelte';
	
	// let data;

	let promise = getData();

	async function getData() {
		const apiURL = 'https://rz6xb697g4.execute-api.eu-west-2.amazonaws.com/production/twdelivery';

		const res = await fetch(apiURL, {
	      headers: { 'Access-Control-Allow-Origin': '*' }
	    });

		const text = await res.text();

		if (res.ok) {
			return text;
		} else {
			throw new Error(text);
		}
	}

	// onMount(async () => {
	// 	const apiURL = 'https://rz6xb697g4.execute-api.eu-west-2.amazonaws.com/production/twdelivery';

	// 	const res = await fetch(apiURL);

	// 	data = [...await res.json()];

	// });

</script>

{#await promise}
	<p>...waiting</p>
{:then data}
	<Content content={data} />
{:catch error}
	<p style="color: red">{error.message}</p>
{/await}
