<script lang="ts">
	export let program: {
		length: number | string;
		rating: string;
		curriculum: string;
		classes: string;
	};
</script>

<div class="bg-gray-900 pt-12 sm:pt-16">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="max-w-4xl mx-auto text-center">
			<h2 class="text-3xl sm:text-4xl font-extrabold text-gray-100">
				Trusted by developers from over 80+ planets
			</h2>
			<p class="mt-3 text-xl text-indigo-50 sm:mt-4">Something right here yeah sure it is</p>
		</div>
	</div>
	<div class="mt-10 pb-12 sm:pb-16 bg-white">
		<div class="relative">
			<div class="absolute inset-0 h-1/2 bg-gray-900"></div>
			<div class="relative mam-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
				<div class="max-w-5xl mx-auto">
					<dl class="rounded-lg bg-white shadow-lg sm:grid sm:grid-cols-4">
						<div
							class="flex flex-col border-b border-gray-100 p-6 text-center sm:border-0 sm:border-r"
						>
							<dt class="order-2 mt-2 text-lg leading-6 font-medium text-gray-500">Length</dt>
							<dd
								class="order-1 text-4xl font-extrabold text-indigo-600 flex items-center justify-center gap-1"
							>
								{program.length}
								<span class="text-xs font-normal tracking-wide bg-indigo-100 px-2 py-px rounded"
									>weeks</span
								>
							</dd>
						</div>
						<div
							class="flex flex-col border-b border-t border-gray-100 p-6 text-center sm:border-0 sm:border-l sm:border-r"
						>
							<dt class="order-2 mt-2 text-lg leading-6 font-medium text-gray-500">Rating</dt>
							<dd
								class="order-1 text-4xl font-extrabold text-indigo-600 flex items-center justify-center"
							>
								{program.rating}
								<svg
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke-width="1.5"
									stroke="currentColor"
									class="w-6 h-6 fill-yellow-200 stroke-black"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M11.48 3.499a.562.562 0 0 1 1.04 0l2.125 5.111a.563.563 0 0 0 .475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 0 0-.182.557l1.285 5.385a.562.562 0 0 1-.84.61l-4.725-2.885a.562.562 0 0 0-.586 0L6.982 20.54a.562.562 0 0 1-.84-.61l1.285-5.386a.562.562 0 0 0-.182-.557l-4.204-3.602a.562.562 0 0 1 .321-.988l5.518-.442a.563.563 0 0 0 .475-.345L11.48 3.5Z"
									/>
								</svg>
							</dd>
						</div>
						<div
							class="flex flex-col border-b border-t border-gray-100 p-6 text-center sm:border-0 sm:border-l sm:border-r"
						>
							<dt class="order-2 mt-2 text-lg leading-6 font-medium text-gray-500">Curriculum</dt>
							<dd class="order-1 text-4xl font-extrabold text-indigo-600">{program.curriculum}</dd>
						</div>
						<div
							class="flex flex-col border-t border-gray-100 p-6 text-center sm:border-0 sm:border-l"
						>
							<dt class="order-2 mt-2 text-lg leading-6 font-medium text-gray-500">Classes</dt>
							<dd class="order-1 text-4xl font-extrabold text-indigo-600">{program.classes}</dd>
						</div>
					</dl>
				</div>
			</div>
		</div>
	</div>
</div>
