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

	let currentTab = 0;
	const setCurrentTab = (x: number) => (currentTab = x);
	const tabs = [
		{
			title: 'Foundations',
			description:
				'The Foundations unit consists of lessons on HTML, CSS, and Javascript. These are the core technologies used in modern web development. These lessons are designed to help all pioneers of any skill level. The Foundations curriculum covers the basics of programming through the more advanced concepts.',
			curriculum: [
				'HTML - the foundation of web development',
				'CSS - making your web sites look great',
				'Javascript - giving functionality to your web sites',
				'Git - Version Control System to save your progress'
			],
			features: [
				'Supports pioneers of all skill levels',
				'Hands-on learning approach. Learn by practicing your skills.',
				'Industry-experienced instructors',
				'Immersive learning experience',
				'Unit concludes with a wrap-up project to showcase your skills'
			]
		},
		{ title: 'Front-end Development', description: '', curriculum: [], features: [] },
		{ title: 'Back-end Development', description: '', curriculum: [], features: [] },
		{ title: 'Full Stack Development', description: '', curriculum: [], features: [] }
	];
</script>

<main>
	<ProgramsHeader {program} />
	<ProgramStats {program} />
	<div class="bg-white py-16 sm:py-24">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="grid grid-cols-12 gap-4">
				<div class="gap-y-10 sm:gap-x-4 grid grid-cols-12 col-span-12">
					<div class="relative hidden lg:block col-span-3">
						<aside class="top-[10%] sticky">
							<h2 class="text-sm font-medium mb-3 text-indigo-700">Blaze Your Trail</h2>
							<nav class="bg-white border border-gray-200 rounded-lg">
								<ul role="navigation" class="divide-y-2 border-b-2 border-inherit divide-inherit">
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal">Overview</a>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal"
											>DevPioneer Institute Experience</a
										>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal"
											>Learning Trail</a
										>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal">Tuition</a>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal"
											>Hands-on Projects</a
										>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal">Schedule</a>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal"
											>Pair Programming</a
										>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal"
											>Job Placement</a
										>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal">Admissions</a>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal"
											>Testimonials</a
										>
									</li>
									<li class="grid">
										<a href="#" class=" inline-block px-6 py-3 text-base font-normal">FAQs</a>
									</li>
								</ul>
								<div class="py-4 px-6 grid">
									<a
										href="/admissions"
										class="inline-block py-2 px-4 bg-indigo-600 text-white text-base text-center font-medium rounded-md hover:bg-indigo-700/75 tracking-widest uppercase"
										>Enroll now</a
									>
								</div>
							</nav>
						</aside>
					</div>
					<div class="col-span-12 lg:col-span-8 lg:col-start-5">
						<div class="max-w-3xl">
							<h2 class="text-3xl sm:text-4xl font-extrabold text-indigo-700">
								The DevPioneer Institute Experience
							</h2>
							<p class="text-base mt-6">
								DevPioneer Institutes full-time program is an immersive and rigorous 15 week
								hands-on course. For those brave pioneers seeking a rewarding career quickly.
							</p>
						</div>
						<div class="mt-6 pb-12 sm:pb-24 max-w-3xl">
							<p class="text-xl sm:text-2xl font-extrabold text-gray-900">
								The Full-time program highlights
							</p>
							<div class="mt-6 grid grid-cols-2 gap-6 items-start">
								<div class="grid col-span-2 lg:col-span-1 space-y-2">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="w-6 h-6"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M11.48 3.499a.562.562 0 0 1 1.04 0l2.125 5.111a.563.563 0 0 0 .475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 0 0-.182.557l1.285 5.385a.562.562 0 0 1-.84.61l-4.725-2.885a.562.562 0 0 0-.586 0L6.982 20.54a.562.562 0 0 1-.84-.61l1.285-5.386a.562.562 0 0 0-.182-.557l-4.204-3.602a.562.562 0 0 1 .321-.988l5.518-.442a.563.563 0 0 0 .475-.345L11.48 3.5Z"
										/>
									</svg>
									<h3 class="text-lg font-medium">Top rated full-time program</h3>
									<p class="text-base text-gray-500">
										DevPioneer Institute is a top rated coding program and our students and alumni
										show this.
									</p>
								</div>
								<div class="grid col-span-2 lg:col-span-1 space-y-2">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="w-6 h-6"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M12 6v6h4.5m4.5 0a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
										/>
									</svg>

									<h3 class="text-lg font-medium">Dedicated teachers and staff</h3>
									<p class="text-base text-gray-500">
										Get hired with the support of our industry professionals. Designed to optimize
										your interpersonal skills and build an ideal web developer career for you.
									</p>
								</div>
								<div class="grid col-span-2 lg:col-span-1 space-y-2">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="w-6 h-6"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="m6.75 7.5 3 2.25-3 2.25m4.5 0h3m-9 8.25h13.5A2.25 2.25 0 0 0 21 18V6a2.25 2.25 0 0 0-2.25-2.25H5.25A2.25 2.25 0 0 0 3 6v12a2.25 2.25 0 0 0 2.25 2.25Z"
										/>
									</svg>

									<h3 class="text-lg font-medium">Experienced Instructors</h3>
									<p class="text-base text-gray-500">
										Our instructors are experienced industry professionals with a passion for
										programming. Having worked for Fortune 500 companies to glorified start-ups
										they've seen it all.
									</p>
								</div>
								<div class="grid col-span-2 lg:col-span-1 space-y-2">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="w-6 h-6"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M10.125 2.25h-4.5c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125v-9M10.125 2.25h.375a9 9 0 0 1 9 9v.375M10.125 2.25A3.375 3.375 0 0 1 13.5 5.625v1.5c0 .621.504 1.125 1.125 1.125h1.5a3.375 3.375 0 0 1 3.375 3.375M9 15l2.25 2.25L15 12"
										/>
									</svg>

									<h3 class="text-lg font-medium">In demand Curriculum</h3>
									<p class="text-base text-gray-500">
										Job ready when you graduate. Our immersive curriculum will get you ready for the
										jobs of today and tomorrow.
									</p>
								</div>
								<div class="grid col-span-2 lg:col-span-1 space-y-2">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="w-6 h-6"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M14.25 9.75 16.5 12l-2.25 2.25m-4.5 0L7.5 12l2.25-2.25M6 20.25h12A2.25 2.25 0 0 0 20.25 18V6A2.25 2.25 0 0 0 18 3.75H6A2.25 2.25 0 0 0 3.75 6v12A2.25 2.25 0 0 0 6 20.25Z"
										/>
									</svg>

									<h3 class="text-lg font-medium">Modern Coding Tools</h3>
									<p class="text-base text-gray-500">
										Use popular developer tools like Visual Studio Code, Git, and Chrome Dev Tools.
									</p>
								</div>
								<div class="grid col-span-2 lg:col-span-1 space-y-2">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										fill="none"
										viewBox="0 0 24 24"
										stroke-width="1.5"
										stroke="currentColor"
										class="w-6 h-6"
									>
										<path
											stroke-linecap="round"
											stroke-linejoin="round"
											d="M18 18.72a9.094 9.094 0 0 0 3.741-.479 3 3 0 0 0-4.682-2.72m.94 3.198.001.031c0 .225-.012.447-.037.666A11.944 11.944 0 0 1 12 21c-2.17 0-4.207-.576-5.963-1.584A6.062 6.062 0 0 1 6 18.719m12 0a5.971 5.971 0 0 0-.941-3.197m0 0A5.995 5.995 0 0 0 12 12.75a5.995 5.995 0 0 0-5.058 2.772m0 0a3 3 0 0 0-4.681 2.72 8.986 8.986 0 0 0 3.74.477m.94-3.197a5.971 5.971 0 0 0-.94 3.197M15 6.75a3 3 0 1 1-6 0 3 3 0 0 1 6 0Zm6 3a2.25 2.25 0 1 1-4.5 0 2.25 2.25 0 0 1 4.5 0Zm-13.5 0a2.25 2.25 0 1 1-4.5 0 2.25 2.25 0 0 1 4.5 0Z"
										/>
									</svg>

									<h3 class="text-lg font-medium">Culture of Collaboration</h3>
									<p class="text-base text-gray-500">
										Work with other pioneers to improve your code through code reviews and learn how
										to present it at the same time.
									</p>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16">
							<div class="max-w-3xl space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Blaze your trail
								</h2>
								<p class="text-base">
									These are the in demand technologies you will learn on your journey.
								</p>
								<p class="text-base">
									Classes are held <span class="font-bold">every weekday</span>, Monday through
									Friday, from 10:00am - 5:00pm
								</p>
								<div class="border border-gray-200 rounded-md shadow-sm">
									<div class="sm:hidden p-2">
										<label for="tabs" class="sr-only">Select a tab</label>
										<div class="relative grid grid-cols-1 items-center">
											<select
												on:change={(e) => setCurrentTab(Number(e.currentTarget.value))}
												bind:value={currentTab}
												name="tabs"
												id="tabs"
												class="col-start-1 block w-full appearance-none bg-none border border-gray-200 rounded-md py-4 px-2 focus:outline-none focus:border-indigo-700"
											>
												<option value={0}>Foundations</option>
												<option value={1}>Front-end Development</option>
												<option value={2}>Back-end Development</option>
												<option value={3}>Full Stack Development</option>
											</select>
											<span class="absolute col-start-1 right-2 pointer-events-none">
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke-width="1.5"
													stroke="currentColor"
													class="w-6 h-6"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														d="m19.5 8.25-7.5 7.5-7.5-7.5"
													/>
												</svg>
											</span>
										</div>
									</div>
									<div class="hidden sm:block">
										<div class="rounded-t-md bg-gray-50">
											<nav class="flex border-b border-gray-200" aria-label="Tabs">
												<button
													on:click={() => setCurrentTab(0)}
													type="button"
													class="w-0 flex-1 py-4 px-1 border-b-2"
													class:border-transparent={currentTab !== 0}
													class:border-indigo-700={currentTab === 0}>Foundations</button
												>
												<button
													type="button"
													class="w-0 flex-1 py-4 px-1 border-b-2"
													class:border-transparent={currentTab !== 1}
													class:border-indigo-700={currentTab === 1}
													on:click={() => setCurrentTab(1)}>Front-end Development</button
												>
												<button
													type="button"
													class="w-0 flex-1 py-4 px-1 border-b-2"
													class:border-indigo-700={currentTab === 2}
													class:border-transparent={currentTab !== 2}
													on:click={() => setCurrentTab(2)}>Back-end Development</button
												>
												<button
													type="button"
													class="w-0 flex-1 py-4 px-1 border-b-2"
													class:border-indigo-700={currentTab === 3}
													class:border-transparent={currentTab !== 3}
													on:click={() => setCurrentTab(3)}>Full Stack Development</button
												>
											</nav>
										</div>
									</div>
									<div class="p-6 space-y-6">
										<p class="text-2xl">{tabs[currentTab].title}</p>
										<p class="text-base">{tabs[currentTab].description}</p>
										<p class="text-lg font-semibold">
											{tabs[currentTab].title} curriculum includes:
										</p>
										<ul class="space-y-6">
											{#each tabs[currentTab].curriculum as item}
												<li class="flex gap-2">
													<svg
														xmlns="http://www.w3.org/2000/svg"
														fill="none"
														viewBox="0 0 24 24"
														stroke-width="1.5"
														stroke="currentColor"
														class="w-6 h-6"
													>
														<path
															stroke-linecap="round"
															stroke-linejoin="round"
															d="m4.5 12.75 6 6 9-13.5"
														/>
													</svg>
													<p>{item}</p>
												</li>
											{/each}
										</ul>
										<p class="text-lg font-semibold">
											{tabs[currentTab].title} features:
										</p>
										<ul class="space-y-6">
											{#each tabs[currentTab].features as item}
												<li class="flex gap-2">
													<svg
														xmlns="http://www.w3.org/2000/svg"
														fill="none"
														viewBox="0 0 24 24"
														stroke-width="1.5"
														stroke="currentColor"
														class="w-6 h-6"
													>
														<path
															stroke-linecap="round"
															stroke-linejoin="round"
															d="m4.5 12.75 6 6 9-13.5"
														/>
													</svg>
													<p>{item}</p>
												</li>
											{/each}
										</ul>
									</div>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16">
							<div class="max-w-3xl space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">Tuition</h2>
								<p>
									At DevPioneer Institute we strive to make our education more accessible to our
									pioneers.
								</p>
								<div class="bg-white shadow overflow-hidden rounded-md">
									<ul role="list" class="divide-y divide-gray-200">
										<div class="px-6 py-4">
											<p class="text-lg">
												The full-time program tuition is <span
													class="text-lg font-semibold text-indigo-700 tracking-tight">$22,000</span
												>
											</p>
											<p class="text-sm mt-1 text-gray-400 italic max-w-xl">
												*A refundable deposit of $99, applied to your total tuition, is due at the
												time of enrollment. The deposit is refundable up until the end of the first
												week of classes.*
											</p>
										</div>
										<div class="px-6 py-4">
											<p class="text-lg">
												There are a number of ways a pioneer can decide to fund their future career
												in tech. Ways include self-payments, employer-payments, bank loans,
												scholarships, and educational grants
											</p>
										</div>
										<div class="px-6 py-4 space-y-1">
											<p class="text-lg">Payment Plans</p>
											<p class="text-base">As Low As</p>
											<p class="text-xl font-bold">$300/month</p>
										</div>
										<div class="px-6 py-4">
											<a
												href="#"
												class="text-indigo-700 hover:text-indigo-600 font-medium underline"
												>View all payment options</a
											>
										</div>
									</ul>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16">
							<div class="max-w-3xl">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Hands-on Projects
								</h2>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</main>
