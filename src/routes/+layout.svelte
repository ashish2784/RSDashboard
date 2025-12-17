<script>
	import favicon from '$lib/assets/rs logo.jpeg';
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

<main>
	
</main>
