<script lang="ts">
	import Careers from '$lib/components/Careers.svelte';
	import LogoCloud from '$lib/components/LogoCloud.svelte';
	import StartHere from '$lib/components/StartHere.svelte';
</script>

<main>
	<div class="bg-gradient-to-r from-purple-800 to-indigo-700 relative">
		<div class="absolute inset-0">
			<div class="grid grid-cols-2 grid-rows-1 h-full">
				<div class="col-span-2 lg:col-span-1 lg:col-start-2">
					<img
						src="images/pairprogram.jpg"
						alt=""
						class="w-full h-full object-cover object-right mix-blend-multiply grayscale opacity-25 lg:opacity-100"
					/>
				</div>
			</div>
		</div>
		<div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="py-24 grid items-center lg:grid-cols-2 lg:gap-6">
				<div class="space-y-6">
					<h1 class="text-5xl lg:text-6xl text-white font-extrabold tracking-wide max-w-lg">
						This is DevPioneer Institute
					</h1>
					<p class="text-xl text-indigo-200 max-w-lg">
						DevPioneer Institute prepares students for fulfilling careers in tech with an innovative
						and immersive curriculum. Offering full-time, part-time, and online programs to fit
						everyones different life schedules.
					</p>
				</div>
			</div>
		</div>
	</div>
	<div class="py-24">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="grid grid-cols-6 gap-6">
				<div class="col-span-6 lg:col-span-2">
					<h2 class="text-4xl font-semibold">Why DevPioneer Institute?</h2>
					<p class="mt-2 text-2xl font-medium text-indigo-700">Highly Acclaimed</p>
					<p class="mt-2 text-lg max-w-lg">
						Our immersive curriculum prepares students to work with industry leading tech giants,
						innovative startups, and organizations of all sizes. Our graduates have contributed to
						the success of many of these businesses with the skills they learned right here with
						DevPioneer Institute.
					</p>
				</div>
				<div class="col-span-6 md:col-span-4 lg:col-span-3 lg:col-start-4">
					<img src="images/hero1.jpg" alt="class full of eager students" />
				</div>
			</div>
		</div>
	</div>
	<div class="py-24">
		<LogoCloud />
	</div>
	<div class="py-24">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="grid grid-cols-6 gap-6">
				<div class="col-span-6 md:col-start-3 md:col-span-4 lg:col-span-3">
					<img src="images/hero2.jpg" alt="office meeting" />
				</div>
				<div class="col-span-6 md:col-start-3 lg:col-start-5 lg:col-span-2">
					<h2 class="text-4xl font-semibold max-w-lg">DevPioneer Institute Experience</h2>
					<p class="mt-2 text-2xl font-medium text-indigo-700">Revolutionizing the industry</p>
					<p class="mt-2 text-lg max-w-lg">
						At DevPioneer Institute we provide our graduates with the necessary skills to transform
						the workforce. From the classroom to the boardroom. A DevPioneer Institute graduate is
						prepared to enter the workforce immediately after graduating.
					</p>
				</div>
			</div>
		</div>
	</div>
	<div class="bg-indigo-700 pt-24 pb-6">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<h2 class="text-4xl font-semibold text-white">Find the Right Program for you</h2>
		</div>
	</div>
	<div class="relative mb-24">
		<div class="absolute inset-x-0 top-0 h-24 bg-indigo-700"></div>
		<div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="grid grid-cols-3 gap-x-4 gap-y-8 lg:gap-6">
				<div
					class="md:col-span-2 lg:col-span-1 col-span-3 border border-gray-200 rounded-lg overflow-hidden group transition-shadow hover:shadow-lg grid grid-rows-[auto_1fr_auto] bg-white"
				>
					<div class="h-40 overflow-hidden">
						<img
							src="/images/part-time.jpg"
							alt="woman sitting at computer working"
							class="w-full h-full object-cover transition-transform group-hover:scale-105"
						/>
					</div>
					<div class="p-6 space-y-2">
						<p class="text-2xl font-semibold">Part-time Program</p>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Code Review</p>
						</div>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Pair programming</p>
						</div>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Interview Prep</p>
						</div>
					</div>
					<div class="grid border-t border-gray-200 text-center p-6">
						<a
							href="/programs/part-time"
							class="bg-gray-100 p-3 border rounded-lg tracking-widest font-medium hover:bg-gray-200"
							>Learn More</a
						>
					</div>
				</div>
				<div
					class="md:col-span-2 md:col-start-2 lg:col-span-1 lg:col-start-auto col-span-3 border border-gray-200 rounded-lg overflow-hidden group transition-shadow hover:shadow-lg grid grid-rows-[auto_1fr_auto] bg-white"
				>
					<div class="h-40 overflow-hidden">
						<img
							src="/images/full-time.jpg"
							alt="woman sitting at computer working"
							class="w-full h-full object-cover transition-transform group-hover:scale-105"
						/>
					</div>
					<div class="p-6 space-y-2">
						<p class="text-2xl font-semibold">Full-time Program</p>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Interview Prep</p>
						</div>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Job Placement</p>
						</div>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>One-on-one Mentorship</p>
						</div>
					</div>
					<div class="grid border-t border-gray-200 text-center p-6">
						<a
							href="/programs/full-time"
							class="bg-gray-100 p-3 border rounded-lg tracking-widest font-medium hover:bg-gray-200"
							>Learn More</a
						>
					</div>
				</div>
				<div
					class="md:col-span-2 lg:col-span-1 col-span-3 border border-gray-200 rounded-lg overflow-hidden group transition-shadow hover:shadow-lg grid grid-rows-[auto_1fr_auto] bg-white"
				>
					<div class="h-40 overflow-hidden">
						<img
							src="/images/programs.jpg"
							alt="woman sitting at computer working"
							class="w-full h-full object-cover transition-transform group-hover:scale-105"
						/>
					</div>
					<div class="p-6 space-y-2">
						<p class="text-2xl font-semibold">Online Program</p>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Same Curriculum</p>
						</div>
						<div class="flex items-center gap-2">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6 text-green-500"
							>
								<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
							</svg>
							<p>Self Paced</p>
						</div>
					</div>
					<div class="grid border-t border-gray-200 text-center p-6">
						<a
							href="/programs/full-time"
							class="bg-gray-100 p-3 border rounded-lg tracking-widest font-medium hover:bg-gray-200"
							>Learn More</a
						>
					</div>
				</div>
			</div>
		</div>
	</div>
	<Careers />
	<StartHere />
</main>
