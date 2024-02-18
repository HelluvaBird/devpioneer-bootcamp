<script lang="ts">
	export let program: {
		title: string;
		subtitle: string;
		length: number | string;
	};
</script>

<div class="relative bg-indigo-700">
	<div class="absolute inset-0">
		<img
			src="/images/programs.jpg"
			alt="three people sitting at a table while studying"
			class="w-full h-full object-cover filter grayscale"
		/>
		<div class="absolute inset-0 bg-indigo-700 mix-blend-multiply" aria-hidden="true"></div>
	</div>
	<div class="relative max-w-7xl mx-auto py-24 sm:py-32 px-4 sm:px-6 lg:px-8">
		<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight text-white">
			{program.title}
		</h1>
		<p class="mt-6 text-xl text-indigo-200 max-w-3xl">{program.subtitle}</p>
		<div class="mt-6 max-w-xl flow-root">
			<ul role="list">
				<li>
					<div class="relative pb-8">
						<span class="absolute top-4 left-4 -ml-px h-full w-0.5 bg-indigo-200" aria-hidden="true"
						></span>
						<div class="relative flex space-x-4">
							<div>
								<span
									class="h-8 w-8 rounded-full bg-purple-600 flex items-center justify-center ring-2 ring-indigo-200"
								>
									<svg
										class="h-5 w-5 text-white"
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
											clip-rule="evenodd"
										/>
									</svg>
								</span>
							</div>
							<div class="min-w-0 flex-1 pt-1.5 space-x-4">
								<p class="text-sm text-white">
									Enrolled in <span class="font-medium text-indigo-200">DevPioneer Institute</span>
								</p>
							</div>
						</div>
					</div>
				</li>
				<li>
					<div class="relative pb-8">
						<span class="absolute top-4 left-4 -ml-px h-full w-0.5 bg-indigo-200" aria-hidden="true"
						></span>
						<div class="relative flex space-x-4">
							<div>
								<span
									class="h-8 w-8 rounded-full bg-purple-600 flex items-center justify-center ring-2 ring-indigo-200"
								>
									<svg
										class="h-5 w-5 text-white"
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											d="M2 10.5a1.5 1.5 0 113 0v6a1.5 1.5 0 01-3 0v-6zM6 10.333v5.43a2 2 0 001.106 1.79l.05.025A4 4 0 008.943 18h5.416a2 2 0 001.962-1.608l1.2-6A2 2 0 0015.56 8H12V4a2 2 0 00-2-2 1 1 0 00-1 1v.667a4 4 0 01-.8 2.4L6.8 7.933a4 4 0 00-.8 2.4z"
										/>
									</svg>
								</span>
							</div>
							<div class="min-w-0 flex-1 pt-1.5">
								<p class="text-sm text-white">
									Blaze your tech trail in <span class="font-medium text-indigo-200"
										>{program.title}</span
									>
								</p>
							</div>
						</div>
					</div>
				</li>
				<li>
					<div class="relative pb-8">
						<span class="absolute top-4 left-4 -ml-px h-full w-0.5 bg-indigo-200" aria-hidden="true"
						></span>
						<div class="relative flex space-x-4">
							<div>
								<span
									class="h-8 w-8 rounded-full bg-purple-600 flex items-center justify-center ring-2 ring-indigo-200"
								>
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="h-5 w-5 text-white"
										aria-hidden="true"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M4.26 10.147a60.438 60.438 0 0 0-.491 6.347A48.62 48.62 0 0 1 12 20.904a48.62 48.62 0 0 1 8.232-4.41 60.46 60.46 0 0 0-.491-6.347m-15.482 0a50.636 50.636 0 0 0-2.658-.813A59.906 59.906 0 0 1 12 3.493a59.903 59.903 0 0 1 10.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.717 50.717 0 0 1 12 13.489a50.702 50.702 0 0 1 7.74-3.342M6.75 15a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Zm0 0v-3.675A55.378 55.378 0 0 1 12 8.443m-7.007 11.55A5.981 5.981 0 0 0 6.75 15.75v-1.5"
										/>
									</svg>
								</span>
							</div>
							<div class="min-w-0 flex-1 pt-1.5">
								<p class="text-sm text-white">
									Complete immersive curriculum in <span class="font-medium text-indigo-200"
										>{program.length} weeks</span
									>
								</p>
							</div>
						</div>
					</div>
				</li>
				<li>
					<div class="relative pb-8">
						<span class="absolute top-4 left-4 -ml-px h-full w-0.5 bg-indigo-200" aria-hidden="true"
						></span>
						<div class="relative flex space-x-4">
							<div>
								<span
									class="h-8 w-8 rounded-full bg-purple-600 flex items-center justify-center ring-2 ring-indigo-200"
								>
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="h-5 w-5 text-white"
										aria-hidden="true"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m6.75 12-3-3m0 0-3 3m3-3v6m-1.5-15H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z"
										/>
									</svg>
								</span>
							</div>
							<div class="min-w-0 flex-1 pt-1.5">
								<p class="text-sm text-white">
									Apply for <span class="font-medium text-indigo-200">Front End Developer</span>
								</p>
							</div>
						</div>
					</div>
				</li>
				<li>
					<div class="relative pb-8">
						<div class="relative flex space-x-4">
							<div>
								<span
									class="h-8 w-8 rounded-full bg-purple-600 flex items-center justify-center ring-2 ring-indigo-200"
								>
									<svg
										class="h-5 w-5 text-white"
										xmlns="http://www.w3.org/2000/svg"
										viewBox="0 0 20 20"
										fill="currentColor"
										aria-hidden="true"
									>
										<path
											fill-rule="evenodd"
											d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
											clip-rule="evenodd"
										/>
									</svg>
								</span>
							</div>
							<div class="min-w-0 flex-1 pt-1.5">
								<p class="text-sm text-white">
									Hired as <span class="font-medium text-indigo-200">Front End Developer</span>
								</p>
							</div>
						</div>
					</div>
				</li>
			</ul>
		</div>
	</div>
</div>
