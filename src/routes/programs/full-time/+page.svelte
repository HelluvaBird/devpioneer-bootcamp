<script lang="ts">
	import ProgramStats from '$lib/components/ProgramStats.svelte';
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	const program = {
		title: 'Full-time Program',
		subtitle: 'For brave pioneers looking for an intense and immersive experience.',
		length: 15,
		rating: '4.8',
		curriculum: 'Javascript',
		classes: 'Weekdays'
	};
</script>

<main>
	<ProgramsHeader {program} />
	<ProgramStats {program} />
</main>
