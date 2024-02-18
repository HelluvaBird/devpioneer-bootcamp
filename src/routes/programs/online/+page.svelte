<script lang="ts">
	import ProgramStats from '$lib/components/ProgramStats.svelte';
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	const program = {
		title: 'Online Program',
		subtitle: 'Blaze your trail with our top rated online cirriculum.',
		length: '15-30',
		rating: '4.8',
		curriculum: 'Javascript',
		classes: 'Online'
	};
</script>

<main>
	<ProgramsHeader {program} />
	<ProgramStats {program} />
</main>
