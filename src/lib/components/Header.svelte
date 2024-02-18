<script lang="ts">
	let programsMenuOpen = false;
	let mobileMenuOpen = false;
	let menuContainer: HTMLDivElement;
	let mobileMenuContainer: HTMLDivElement;
	let firstMobileLink: HTMLAnchorElement;

	function onWindowClick(e: MouseEvent) {
		if (!programsMenuOpen) return;
		if (e.target instanceof HTMLElement && !menuContainer.contains(e.target)) {
			programsMenuOpen = false;
		}
	}

	function onWindowClickMobile(e: MouseEvent) {
		if (!mobileMenuOpen) return;
		if (e.target instanceof HTMLElement && !mobileMenuContainer.contains(e.target)) {
			mobileMenuOpen = false;
		}
	}

	function onMenuBlur(e: FocusEvent) {
		requestAnimationFrame(() => {
			if (
				e.relatedTarget instanceof HTMLElement &&
				!menuContainer.contains(document.activeElement)
			) {
				programsMenuOpen = false;
			}
		});
	}
</script>

<svelte:window on:click={onWindowClick} on:click={onWindowClickMobile} />

<header class="bg-white">
	<nav class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div
			class="w-full py-6 flex flex-wrap gap-y-4 sm:gap-y-0 items-center justify-between border-b border-gray-500 lg:border-none"
		>
			<div class="flex items-center">
				<a href="/" class="text-base font-semibold">DevPioneer Institute</a>
				<div class="hidden ml-10 space-x-8 lg:block">
					<div
						role="navigation"
						class="relative inline"
						bind:this={menuContainer}
						on:focusout={onMenuBlur}
					>
						<button
							on:click={() => (programsMenuOpen = !programsMenuOpen)}
							type="button"
							class="group inline-flex items-center text-base font-medium bg-white appearance-none border border-transparent rounded-sm text-gray-400 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
						>
							<span>Programs</span>
							<svg
								class="text-gray-400 ml-2 h-5 w-5 group-hover:text-gray-900"
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
							>
								<path
									fill-rule="evenodd"
									d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
									clip-rule="evenodd"
								/>
							</svg>
						</button>
						{#if programsMenuOpen}
							<div
								class="absolute z-10 w-screen max-w-md top-10 left-1/2 transform -translate-x-1/2"
							>
								<div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-10 overflow-hidden">
									<div class="relative grid gap-6 bg-white px-5 py-6 sm:gap-8 sm:p-8">
										<a
											href="/programs/full-time"
											class="p-3 flex flex-col items-start rounded-lg hover:bg-gray-50"
										>
											<p class="text-base font-medium text-gray-900">Full-time Program</p>
											<p class="text-gray-500 text-sm mt-1">
												For brave pioneers looking for an intense and immersive experience.
											</p>
										</a>
										<a
											href="/programs/part-time"
											class="p-3 flex flex-col items-start rounded-lg hover:bg-gray-50"
										>
											<p class="text-base font-medium text-gray-900">Part-time Program</p>
											<p class="text-gray-500 text-sm mt-1">
												For busy pioneers or for those looking to make a career change into tech.
											</p>
										</a>
										<a
											href="/programs/online"
											class="p-3 flex flex-col items-start rounded-lg hover:bg-gray-50"
										>
											<p class="text-base font-medium text-gray-900">Online Program</p>
											<p class="text-gray-500 text-sm mt-1">
												Blaze your trail with our top rated online cirriculum.
											</p>
										</a>
									</div>
								</div>
							</div>
						{/if}
					</div>
					<a href="/price" class="text-base font-medium text-gray-400 hover:text-gray-900">Price</a>
					<a href="/admissions" class="text-base font-medium text-gray-400 hover:text-gray-900"
						>Admissions</a
					>
					<a href="#" class="text-base font-medium text-gray-400 hover:text-gray-900">Support</a>
				</div>
			</div>
			<div class="sm:ml-10 space-x-4">
				<a href="#" class="text-base font-medium text-gray-400 hover:text-gray-900">Sign in</a>
				<a
					href="/admissions"
					class="inline-block bg-indigo-600 text-white py-2 px-4 border border-transparent rounded-md text-base font-medium hover:bg-indigo-700/75"
					>Enroll now</a
				>
			</div>
		</div>
		<div class="py-6 flex flex-wrap justify-center space-x-6 lg:hidden">
			<div class="relative" bind:this={mobileMenuContainer}>
				<button
					on:click={() => (mobileMenuOpen = !mobileMenuOpen)}
					on:focus={() => firstMobileLink.focus()}
					type="button"
					class="group inline-flex items-center text-base font-medium bg-white appearance-none border border-transparent rounded-sm text-gray-400 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
				>
					<span>Programs</span>
					<svg
						class="text-gray-400 ml-2 h-5 w-5 group-hover:text-gray-900"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						aria-hidden="true"
					>
						<path
							fill-rule="evenodd"
							d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
							clip-rule="evenodd"
						/>
					</svg>
				</button>
			</div>
			<a href="/price" class="text-base font-medium text-gray-400 hover:text-gray-900">Price</a>
			<a href="/admissions" class="text-base font-medium text-gray-400 hover:text-gray-900"
				>Admissions</a
			>
			<a href="#" class="text-base font-medium text-gray-400 hover:text-gray-900">Support</a>
		</div>
		<div
			class="absolute inset-x-0 top-full bg-white z-10 grid lg:hidden grid-rows-[0fr] overflow-hidden transition-[grid-template-rows]"
			class:grid-rows-[1fr]={mobileMenuOpen}
		>
			<div class="min-h-0">
				<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 border-t border-gray-200">
					<div class="relative grid gap-6 bg-white px-5 py-6 sm:gap-8 sm:p-8">
						<a
							bind:this={firstMobileLink}
							href="/programs/full-time"
							class="p-3 flex flex-col items-start rounded-lg hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-200"
						>
							<p class="text-base font-medium text-gray-900">Full-time Program</p>
							<p class="text-gray-500 text-sm mt-1">
								For brave pioneers looking for an intense and immersive experience.
							</p>
						</a>
						<a
							href="/programs/part-time"
							class="p-3 flex flex-col items-start rounded-lg hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-200"
						>
							<p class="text-base font-medium text-gray-900">Part-time Program</p>
							<p class="text-gray-500 text-sm mt-1">
								For busy pioneers or for those looking to make a career change into tech.
							</p>
						</a>
						<a
							href="/programs/online"
							class="p-3 flex flex-col items-start rounded-lg hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-200"
						>
							<p class="text-base font-medium text-gray-900">Online Program</p>
							<p class="text-gray-500 text-sm mt-1">
								Blaze your trail with our top rated online cirriculum.
							</p>
						</a>
					</div>
				</div>
			</div>
		</div>
	</nav>
</header>
