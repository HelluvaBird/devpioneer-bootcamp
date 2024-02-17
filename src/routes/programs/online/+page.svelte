<script lang="ts">
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	const program = {
		title: 'Online Program',
		subtitle: 'Blaze your trail with our top rated online cirriculum.',
		length: '15-30'
	};
</script>

<main>
	<ProgramsHeader {program} />
</main>
