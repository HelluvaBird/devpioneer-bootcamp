<script lang="ts">
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	const program = {
		title: 'Part-time Program',
		subtitle: 'For busy pioneers or for those looking to make a career change into tech.',
		length: 30
	};
</script>

<main>
	<ProgramsHeader {program} />
</main>
