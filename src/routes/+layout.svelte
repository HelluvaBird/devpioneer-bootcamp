<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import '../app.css';
</script>

<svelte:head>
	<title>DevPioneer Institute</title>
</svelte:head>

<Header />
<slot />
<Footer />
