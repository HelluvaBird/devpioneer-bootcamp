<script lang="ts">
	let isOpen: boolean = false;

	function toggle() {
		isOpen = !isOpen;
	}

	export let question: string;
	export let answer: string;
</script>

<li class="border border-gray-200 shadow grid">
	<button type="button" class="px-6 py-4 grid" on:click={toggle}>
		<div class="grid grid-cols-[1fr_auto] justify-items-start">
			<span class="font-semibold">{question}</span>
			{#if isOpen}
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
				</svg>
			{:else}
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
				</svg>
			{/if}
		</div>
	</button>
	<div
		class="grid grid-rows-[0fr] overflow-hidden transition-[grid-template-rows] duration-300"
		class:grid-rows-[1fr]={isOpen}
	>
		<div class="min-h-0">
			<p class="p-6 border-t">{answer}</p>
		</div>
	</div>
</li>
