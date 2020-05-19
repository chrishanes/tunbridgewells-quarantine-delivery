<script>
	import Content from '../components/Content.svelte';
	import { get } from 'svelte/store';
	import { twdata } from '../store.js';

	export let data = get(twdata);

</script>

<!-- <script context="module">
	// const apiURL = 'https://st7ot1tu57.execute-api.us-west-2.amazonaws.com/tw-community/community-data';
	const apiURL = 'https://rz6xb697g4.execute-api.eu-west-2.amazonaws.com/production/twdelivery';

	export async function preload({ params, query }) {
		
		const res = await this.fetch(apiURL);
		const data = await res.json();

		return {
			data: data
		}

	}

</script> -->

<Content content={data} />
