<script lang="ts">
	import ProgramStats from '$lib/components/ProgramStats.svelte';
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	const program = {
		title: 'Part-time Program',
		subtitle: 'For busy pioneers or for those looking to make a career change into tech.',
		length: 30,
		rating: '4.8',
		curriculum: 'Javascript',
		classes: 'Evenings'
	};
</script>

<main>
	<ProgramsHeader {program} />
	<ProgramStats {program} />
</main>
