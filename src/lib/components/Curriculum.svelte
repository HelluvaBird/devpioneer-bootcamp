<script lang="ts">
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
		{
			title: 'Front-end Development',
			description:
				'The Front-end Development unit builds upon the Foundations unit. Diving deeper into CSS and JavaScript. We will also get our hands on the popular front-end JavaScript library React. Near the end of the unit pioneers will showcase their front-end skills by building a portfolio web site.',
			curriculum: ['CSS', 'JavaScript', 'React'],
			features: [
				"You'll learn how content and imagery are best displayed on a web site",
				'Hands on the popular JavaScript library React',
				'Working with your fellow pioneers to best optimize your code',
				'Work on a portfolio web site to showcase what you have learned so far'
			]
		},
		{
			title: 'Back-end Development',
			description:
				'The Back-end Development unit will teach how to work with JavaScript on the server by using the JavaScript runtime environment NodeJS. We will also be learning how to communicate with Application Programming Interfaces (APIs) to retrieve vasts amount of data. Finally learning how to store our data in NoSQL and SQL databases.',
			curriculum: ['NodeJS - JavaScript on the back-end', 'APIs', 'MongoDB', 'PostgreSQL'],
			features: [
				'Learn how to plan, research, and build web applications',
				'Help your fellow pioneers with interview preparation and learn how to succeed during an interview',
				'Structure databases appropriately and efficiently',
				'Build a social media web site and develope an E-Commerce platform'
			]
		},
		{
			title: 'Full Stack Development',
			description:
				"The final unit will cover full stack development with the popular React framework NextJS. We will learn the difference between server-rendered and client-rendered components and learn how to use them effectively together. You'll put all your skills to the test when you develop your own SaaS (Software as a Service) web applications as your final project.",
			curriculum: ['React', 'NextJS', 'MongoDB', 'PostgreSQL'],
			features: [
				'Create full stack web applications with NextJS',
				'Demonstrate your front-end and back-end skills',
				'Meet with DevPioneer Institute Career services to begin the search for your new career',
				'Polish your GitHub and LinkedIn profiles to help establish your professional experience',
				'Work with your fellow pioneers on a Full Stack SaaS application'
			]
		}
	];
</script>

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
					<path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
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
						<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
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
						<path stroke-linecap="round" stroke-linejoin="round" d="m4.5 12.75 6 6 9-13.5" />
					</svg>
					<p>{item}</p>
				</li>
			{/each}
		</ul>
	</div>
</div>
