<script lang="ts">
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	const program = {
		title: 'Full-time Program',
		subtitle: 'For brave pioneers looking for an intense and immersive experience.',
		length: 15
	};
</script>

<main>
	<ProgramsHeader {program} />
</main>
