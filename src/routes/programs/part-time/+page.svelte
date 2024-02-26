<script lang="ts">
	import Accordion from '$lib/components/Accordion.svelte';
	import ProgramStats from '$lib/components/ProgramStats.svelte';
	import ProgramsHeader from '$lib/components/ProgramsHeader.svelte';
	import { onMount } from 'svelte';
	const program = {
		title: 'Part-time Program',
		subtitle: 'For busy pioneers or for those looking to make a career change into tech.',
		length: 30,
		rating: '4.8',
		curriculum: 'Javascript',
		classes: 'Evenings'
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
				"The final unit will cover full stack development with the popular React framework NextJS. We will learn the difference between server-rendered and client-rendered components and learn how to use them effectively together. You'll put all your skills to the test when you develope your own SaaS (Software as a Service) web applications as your final project.",
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

	let questions = [
		{
			id: 1,
			question: 'Can I really become a developer in 30 weeks?',
			answer:
				'Absolutely! With our scientifically* proven curriculum and our hands-on mentality the DevPioneer Institute experience will get you job-ready in little as 30 weeks. The part-time program is immersive. It is meant to get you up to speed with industry standards while you work your current job.'
		},
		{
			id: 2,
			question: 'Why should I pursue an education at DevPioneer Institute?',
			answer:
				'As a trusted tech educator we have helped around one hundred brave pioneers graduate job-ready with the skills, persistence, and portfolio to build lasting careers in the tech industry and beyond.'
		},
		{
			id: 3,
			question:
				'Will I need to purchase a computer for this program or will one be provided for me?',
			answer:
				'A computer is required to complete the program. DevPioneer Institute will NOT provide one for you.'
		},
		{
			id: 4,
			question: 'Are there any minimum requirements to apply to the program?',
			answer:
				'DevPioneer Institute welcomes all pioneer prospects to apply. Due to higher education regulations all future pioneers must be 18 years or older and must provide a copy of at least a high school diploma or equivalent.'
		},
		{
			id: 5,
			question: 'Why does DevPioneer Institute choose to teach the program in JavaScript?',
			answer:
				'The future of web development is always evolving. Web sites have become more sophisticated over the years and in order to stay current with development trends, DevPioneer Institute has come to the conclusion JavaScript is the language with the most growth opportunity.'
		},
		{
			id: 6,
			question: 'What types of careers will this program prepare me for?',
			answer:
				'Upon completion of the program graduates will be able to seek employment as Software Developers, Front-end Developers, Full Stack Engineers, and many more tech related fields. '
		}
	];

	onMount(() => {
		const sections = document.querySelectorAll('div[data-scroll-spy]');
		const links = document.querySelectorAll("ul[role='navigation'] li");

		const observer = new IntersectionObserver(
			(entries) => {
				for (const entry of entries) {
					if (entry.isIntersecting) {
						//console.log((entry.target as HTMLElement).dataset.scrollSpy);
						const link = document.querySelector(
							`a[href='#${(entry.target as HTMLElement).dataset.scrollSpy}']`
						);
						links.forEach((el) => (el.className = 'grid'));
						//console.log(link?.parentElement);
						if (link?.parentElement) {
							link.parentElement.className += ' border-s-4 border-s-indigo-700 bg-gray-100';
						}
					}
				}
			},
			{ rootMargin: '-10% 0px -90%' }
		);

		for (const section of sections) {
			observer.observe(section);
		}
	});
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
							<nav class="bg-white border rounded-lg overflow-hidden">
								<ul role="navigation" class="divide-y-2 border-b-2">
									<li class="grid border-s-4 border-s-indigo-700 bg-gray-100">
										<a href="#dpiexperience" class=" inline-block px-6 py-3 text-base font-normal"
											>DevPioneer Institute Experience</a
										>
									</li>
									<li class="grid">
										<a href="#trail" class=" inline-block px-6 py-3 text-base font-normal"
											>Learning Trail</a
										>
									</li>
									<li class="grid">
										<a href="#tuition" class=" inline-block px-6 py-3 text-base font-normal"
											>Tuition</a
										>
									</li>
									<li class="grid">
										<a href="#projects" class=" inline-block px-6 py-3 text-base font-normal"
											>Hands-on Projects</a
										>
									</li>
									<li class="grid">
										<a href="#schedule" class=" inline-block px-6 py-3 text-base font-normal"
											>Schedule</a
										>
									</li>
									<li class="grid">
										<a href="#pairprogram" class=" inline-block px-6 py-3 text-base font-normal"
											>Pair Programming</a
										>
									</li>
									<li class="grid">
										<a href="#careerprep" class=" inline-block px-6 py-3 text-base font-normal"
											>Career Prep</a
										>
									</li>
									<li class="grid">
										<a href="#admissions" class=" inline-block px-6 py-3 text-base font-normal"
											>Admissions</a
										>
									</li>
									<li class="grid">
										<a href="#testimonials" class=" inline-block px-6 py-3 text-base font-normal"
											>Testimonials</a
										>
									</li>
									<li class="grid">
										<a href="#faqs" class=" inline-block px-6 py-3 text-base font-normal">FAQs</a>
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
						<div id="dpiexperience" data-scroll-spy="dpiexperience" class="pb-16">
							<h2 class="max-w-3xl text-3xl sm:text-4xl font-extrabold text-indigo-700">
								The DevPioneer Institute Experience
							</h2>
							<p class="max-w-3xl text-base mt-6">
								DevPioneer Institutes part-time program is an immersive 30 week hands-on course. For
								busy pioneers or for those looking to make a career change into tech.
							</p>
							<div class="mt-6">
								<p class="max-w-3xl text-xl sm:text-2xl font-extrabold text-gray-900">
									The Part-time program highlights
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
										<h3 class="text-lg font-medium">Top rated part-time program</h3>
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
											Job ready when you graduate. Our immersive curriculum will get you ready for
											the jobs of today and tomorrow.
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
											Use popular developer tools like Visual Studio Code, Git, and Chrome Dev
											Tools.
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
											Work with other pioneers to improve your code through code reviews and learn
											how to present it at the same time.
										</p>
									</div>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="trail" data-scroll-spy="trail">
							<div class="space-y-6">
								<h2 class="max-w-3xl text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Blaze your trail
								</h2>
								<p class="max-w-3xl text-base">
									These are the in demand technologies you will learn on your journey.
								</p>
								<p class="max-w-3xl text-base">
									Classes are held <span class="font-bold">Monday, Wednesday, and Friday</span> in the
									evening 7:00pm - 11:00pm
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
								<p class=" italic">
									Class time and schedule options vary by month and are subject to change. To see
									available class times and schedules for the part-time program, complete your
									application.
								</p>
								<p class="text-2xl font-semibold">Why choose the Part-time Program?</p>
								<div class="grid lg:grid-cols-2 gap-x-4 gap-y-8 lg:gap-6 items-start">
									<div class="col-span-2 lg:col-span-1 grid gap-2">
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
												d="M16.5 18.75h-9m9 0a3 3 0 0 1 3 3h-15a3 3 0 0 1 3-3m9 0v-3.375c0-.621-.503-1.125-1.125-1.125h-.871M7.5 18.75v-3.375c0-.621.504-1.125 1.125-1.125h.872m5.007 0H9.497m5.007 0a7.454 7.454 0 0 1-.982-3.172M9.497 14.25a7.454 7.454 0 0 0 .981-3.172M5.25 4.236c-.982.143-1.954.317-2.916.52A6.003 6.003 0 0 0 7.73 9.728M5.25 4.236V4.5c0 2.108.966 3.99 2.48 5.228M5.25 4.236V2.721C7.456 2.41 9.71 2.25 12 2.25c2.291 0 4.545.16 6.75.47v1.516M7.73 9.728a6.726 6.726 0 0 0 2.748 1.35m8.272-6.842V4.5c0 2.108-.966 3.99-2.48 5.228m2.48-5.492a46.32 46.32 0 0 1 2.916.52 6.003 6.003 0 0 1-5.395 4.972m0 0a6.726 6.726 0 0 1-2.749 1.35m0 0a6.772 6.772 0 0 1-3.044 0"
											/>
										</svg>
										<p class="font-semibold">Same top-rated curriculum</p>
										<p>
											Our part-time program offers the same curriculum concepts, projects, and
											career outcomes as our full-time program. All on a 30 week part-time schedule!
										</p>
									</div>
									<div class="col-span-2 lg:col-span-1 grid gap-2">
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
										<p class="font-semibold">Weekday evening classes</p>
										<p>
											Maintain your current job and other responsibilities during the day. Our
											part-time program starts in the evening. Monday, Wednesday, and Fridays from
											7:00pm to 11:00pm
										</p>
									</div>
									<div class="col-span-2 lg:col-span-1 grid gap-2">
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
												d="M12 3v17.25m0 0c-1.472 0-2.882.265-4.185.75M12 20.25c1.472 0 2.882.265 4.185.75M18.75 4.97A48.416 48.416 0 0 0 12 4.5c-2.291 0-4.545.16-6.75.47m13.5 0c1.01.143 2.01.317 3 .52m-3-.52 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.988 5.988 0 0 1-2.031.352 5.988 5.988 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L18.75 4.971Zm-16.5.52c.99-.203 1.99-.377 3-.52m0 0 2.62 10.726c.122.499-.106 1.028-.589 1.202a5.989 5.989 0 0 1-2.031.352 5.989 5.989 0 0 1-2.031-.352c-.483-.174-.711-.703-.59-1.202L5.25 4.971Z"
											/>
										</svg>
										<p class="font-semibold">Class/Work/Life balance</p>
										<p>
											We understand your life is busy. Our set weekly schedule, and committed online
											faculty help to manage the part-time program on top of your existing work
											schedule and other life commitments.
										</p>
									</div>
									<div class="col-span-2 lg:col-span-1 grid gap-2">
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
												d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 0 1 2.25-2.25h13.5A2.25 2.25 0 0 1 21 7.5v11.25m-18 0A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75m-18 0v-7.5A2.25 2.25 0 0 1 5.25 9h13.5A2.25 2.25 0 0 1 21 11.25v7.5m-9-6h.008v.008H12v-.008ZM12 15h.008v.008H12V15Zm0 2.25h.008v.008H12v-.008ZM9.75 15h.008v.008H9.75V15Zm0 2.25h.008v.008H9.75v-.008ZM7.5 15h.008v.008H7.5V15Zm0 2.25h.008v.008H7.5v-.008Zm6.75-4.5h.008v.008h-.008v-.008Zm0 2.25h.008v.008h-.008V15Zm0 2.25h.008v.008h-.008v-.008Zm2.25-4.5h.008v.008H16.5v-.008Zm0 2.25h.008v.008H16.5V15Z"
											/>
										</svg>
										<p class="font-semibold">Consistent Workload</p>
										<p>
											With a consistent workload of lectures, assignments, and projects our
											part-time program provides no unexpected situtations.
										</p>
									</div>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="tuition" data-scroll-spy="tuition">
							<div class="space-y-6">
								<h2 class="max-w-3xl text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Tuition
								</h2>
								<p class="max-w-3xl">
									At DevPioneer Institute we strive to make our education more accessible to our
									pioneers.
								</p>

								<div class="bg-white shadow overflow-hidden rounded-md">
									<ul role="list" class="divide-y divide-gray-200">
										<div class="px-6 py-4">
											<p class="text-lg">
												The part-time program tuition is <span
													class="text-lg font-semibold text-indigo-700 tracking-tight">$12,000</span
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
						<div class="py-16" id="projects" data-scroll-spy="projects">
							<div class="space-y-6">
								<h2 class="max-w-3xl text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Hands-on Projects
								</h2>
								<p class="max-w-3xl text-lg">
									To showcase your technical, and creative skills to future employers we will be
									creating web sites and committing them to the online Git repository GitHub. As you
									conclude each unit a project will be assigned.
								</p>
								<p class="max-w-3xl text-lg">
									These are some of the projects you will be able to work on:
								</p>

								<article class="rounded-xl bg-white p-4 ring ring-indigo-50 sm:p-6 lg:p-8">
									<div class="flex items-start sm:gap-8">
										<div
											class="hidden sm:grid sm:size-20 sm:shrink-0 sm:place-content-center sm:rounded-full sm:border-2 sm:border-indigo-500"
											aria-hidden="true"
										>
											<div class="flex items-center gap-1 text-indigo-500">
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke-width="1.5"
													stroke="currentColor"
													class="w-8 h-8"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														d="M3.75 3v11.25A2.25 2.25 0 0 0 6 16.5h2.25M3.75 3h-1.5m1.5 0h16.5m0 0h1.5m-1.5 0v11.25A2.25 2.25 0 0 1 18 16.5h-2.25m-7.5 0h7.5m-7.5 0-1 3m8.5-3 1 3m0 0 .5 1.5m-.5-1.5h-9.5m0 0-.5 1.5M9 11.25v1.5M12 9v3.75m3-6v6"
													/>
												</svg>
											</div>
										</div>

										<div>
											<strong
												class="rounded border border-indigo-500 bg-indigo-500 px-3 py-1.5 text-[10px] font-medium text-white"
											>
												Project #001
											</strong>

											<h3 class="mt-4 text-lg font-medium sm:text-xl">
												<a href="#" class="hover:underline"> Your portfolio site </a>
											</h3>

											<p class="mt-1 text-sm text-gray-700">
												To showcase the projects you work on to employers. Our first project will be
												your portfolio site. Portfolio web sites are important to demonstrate
												fimilarity with a given language and to show you have the skills needed for
												a role.
											</p>

											<div class="mt-4 sm:flex sm:items-center sm:gap-2">
												<div class="flex items-center gap-1 text-gray-500">
													<svg
														class="h-4 w-4"
														fill="none"
														stroke="currentColor"
														viewBox="0 0 24 24"
														xmlns="http://www.w3.org/2000/svg"
													>
														<path
															stroke-linecap="round"
															stroke-linejoin="round"
															stroke-width="2"
															d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
														></path>
													</svg>

													<p class="text-xs font-medium">4 days</p>
												</div>

												<span class="hidden sm:block" aria-hidden="true">&middot;</span>

												<p class="mt-2 text-xs font-medium text-gray-500 sm:mt-0">
													Technology:
													<span class="text-indigo-500">HTML</span>,
													<span class="text-indigo-500">CSS</span>,
													<span class="text-indigo-500">JavaScript</span>
												</p>
											</div>
										</div>
									</div>
								</article>
								<article class="rounded-xl bg-white p-4 ring ring-indigo-50 sm:p-6 lg:p-8">
									<div class="flex items-start sm:gap-8">
										<div
											class="hidden sm:grid sm:size-20 sm:shrink-0 sm:place-content-center sm:rounded-full sm:border-2 sm:border-indigo-500"
											aria-hidden="true"
										>
											<div class="flex items-center gap-1 text-indigo-500">
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke-width="1.5"
													stroke="currentColor"
													class="w-8 h-8"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														d="M5.25 8.25h15m-16.5 7.5h15m-1.8-13.5-3.9 19.5m-2.1-19.5-3.9 19.5"
													/>
												</svg>
											</div>
										</div>

										<div>
											<strong
												class="rounded border border-indigo-500 bg-indigo-500 px-3 py-1.5 text-[10px] font-medium text-white"
											>
												Project #002
											</strong>

											<h3 class="mt-4 text-lg font-medium sm:text-xl">
												<a href="#" class="hover:underline"> Social Media Platform </a>
											</h3>

											<p class="mt-1 text-sm text-gray-700">
												This project will put your knowledge of the front-end to the test. Social
												media plays a vital role in the world today. Now more than ever content is
												being consumed through social media. Creating a platform of your own is the
												best way to harness that potential.
											</p>

											<div class="mt-4 sm:flex sm:items-center sm:gap-2">
												<div class="flex items-center gap-1 text-gray-500">
													<svg
														class="h-4 w-4"
														fill="none"
														stroke="currentColor"
														viewBox="0 0 24 24"
														xmlns="http://www.w3.org/2000/svg"
													>
														<path
															stroke-linecap="round"
															stroke-linejoin="round"
															stroke-width="2"
															d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
														></path>
													</svg>

													<p class="text-xs font-medium">1-2 weeks</p>
												</div>

												<span class="hidden sm:block" aria-hidden="true">&middot;</span>

												<p class="mt-2 text-xs font-medium text-gray-500 sm:mt-0">
													Technology:
													<span class="text-indigo-500">CSS</span>,
													<span class="text-indigo-500">JavaScript</span>,
													<span class="text-indigo-500">React</span>
												</p>
											</div>
										</div>
									</div>
								</article>
								<article class="rounded-xl bg-white p-4 ring ring-indigo-50 sm:p-6 lg:p-8">
									<div class="flex items-start sm:gap-8">
										<div
											class="hidden sm:grid sm:size-20 sm:shrink-0 sm:place-content-center sm:rounded-full sm:border-2 sm:border-indigo-500"
											aria-hidden="true"
										>
											<div class="flex items-center gap-1 text-indigo-500">
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke-width="1.5"
													stroke="currentColor"
													class="w-8 h-8"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 0 0-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 0 0-16.536-1.84M7.5 14.25 5.106 5.272M6 20.25a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Zm12.75 0a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Z"
													/>
												</svg>
											</div>
										</div>

										<div>
											<strong
												class="rounded border border-indigo-500 bg-indigo-500 px-3 py-1.5 text-[10px] font-medium text-white"
											>
												Project #003
											</strong>

											<h3 class="mt-4 text-lg font-medium sm:text-xl">
												<a href="#" class="hover:underline"> E-Commerce Site </a>
											</h3>

											<p class="mt-1 text-sm text-gray-700">
												After working with NodeJS and connecting the back-end with a database you
												will construct an e-commerce site. This will demonstrate your back-end
												prowess by updating shopping cart components and inventory stocks in a
												database.
											</p>

											<div class="mt-4 sm:flex sm:items-center sm:gap-2">
												<div class="flex items-center gap-1 text-gray-500">
													<svg
														class="h-4 w-4"
														fill="none"
														stroke="currentColor"
														viewBox="0 0 24 24"
														xmlns="http://www.w3.org/2000/svg"
													>
														<path
															stroke-linecap="round"
															stroke-linejoin="round"
															stroke-width="2"
															d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
														></path>
													</svg>

													<p class="text-xs font-medium">2-3 weeks</p>
												</div>

												<span class="hidden sm:block" aria-hidden="true">&middot;</span>

												<p class="mt-2 text-xs font-medium text-gray-500 sm:mt-0">
													Technology:
													<span class="text-indigo-500">NodeJS</span>,
													<span class="text-indigo-500">MongoDB</span>,
													<span class="text-indigo-500">PostgreSQL</span>
												</p>
											</div>
										</div>
									</div>
								</article>
								<article class="rounded-xl bg-white p-4 ring ring-indigo-50 sm:p-6 lg:p-8">
									<div class="flex items-start sm:gap-8">
										<div
											class="hidden sm:grid sm:size-20 sm:shrink-0 sm:place-content-center sm:rounded-full sm:border-2 sm:border-indigo-500"
											aria-hidden="true"
										>
											<div class="flex items-center gap-1 text-indigo-500">
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke-width="1.5"
													stroke="currentColor"
													class="w-8 h-8"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														d="M3 8.25V18a2.25 2.25 0 0 0 2.25 2.25h13.5A2.25 2.25 0 0 0 21 18V8.25m-18 0V6a2.25 2.25 0 0 1 2.25-2.25h13.5A2.25 2.25 0 0 1 21 6v2.25m-18 0h18M5.25 6h.008v.008H5.25V6ZM7.5 6h.008v.008H7.5V6Zm2.25 0h.008v.008H9.75V6Z"
													/>
												</svg>
											</div>
										</div>

										<div>
											<strong
												class="rounded border border-indigo-500 bg-indigo-500 px-3 py-1.5 text-[10px] font-medium text-white"
											>
												Project #004
											</strong>

											<h3 class="mt-4 text-lg font-medium sm:text-xl">
												<a href="#" class="hover:underline"> Software as a Service (SaaS) </a>
											</h3>

											<p class="mt-1 text-sm text-gray-700">
												a web application that is made available over the internet rather than
												software installed on your computers. You will develop your very own SaaS
												and show employers why this software model is beneficial for their
												companies.
											</p>

											<div class="mt-4 sm:flex sm:items-center sm:gap-2">
												<div class="flex items-center gap-1 text-gray-500">
													<svg
														class="h-4 w-4"
														fill="none"
														stroke="currentColor"
														viewBox="0 0 24 24"
														xmlns="http://www.w3.org/2000/svg"
													>
														<path
															stroke-linecap="round"
															stroke-linejoin="round"
															stroke-width="2"
															d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
														></path>
													</svg>

													<p class="text-xs font-medium">2-3 weeks</p>
												</div>

												<span class="hidden sm:block" aria-hidden="true">&middot;</span>

												<p class="mt-2 text-xs font-medium text-gray-500 sm:mt-0">
													Technology: <span class="text-indigo-500">React</span>,
													<span class="text-indigo-500">NextJS</span>,
													<span class="text-indigo-500">MongoDB</span>,
													<span class="text-indigo-500">PostgreSQL</span>
												</p>
											</div>
										</div>
									</div>
								</article>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="schedule" data-scroll-spy="schedule">
							<div class="space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">Daily Schedule</h2>
								<p class="text-lg">
									Our part-time program is an immersive experience. Class is held Monday, Wednesday,
									and Friday from 7pm to 11pm in the evening.
								</p>
								<div class="grid grid-cols-12 gap-8">
									<div class="col-span-12 grid space-y-6">
										<h3 class="text-xl font-extrabold">Activities</h3>
										<p class="text-lg">
											<span class="font-bold">Lecture: </span>Learn from industry experienced
											instructors everyday. They will walk you through practical and theoretical use
											cases. Answer any questions you may have.
										</p>
										<p class="text-lg">
											<span class="font-bold">Pair Programming: </span>Work along with your fellow
											pioneers. Gaining valuable industry experience working as part of a team.
										</p>
										<p class="text-lg">
											<span class="font-bold">Homework: </span>Self-study period to work on your
											assignments, talk to your fellow pioneers, or learn new concepts.
										</p>
									</div>
									<div class="col-span-12">
										<div class="shadow-xl shadow-black/20 p-6 h-full rounded">
											<p class="font-bold text-lg">Your DevPioneer Institute Schedule</p>
											<div class="grid grid-cols-1 gap-y-6 sm:grid-cols-2 mt-6">
												<div class="flex gap-2 items-center">
													<div
														class="size-12 bg-blue-300 border-2 border-dashed border-blue-600 rounded"
													></div>
													<span class="text-blue-600 font-semibold tracking-wide leading-4"
														>Outside of class</span
													>
												</div>
												<div class="flex gap-2 items-center">
													<div
														class="size-12 bg-purple-300 border-2 border-dashed border-purple-600 rounded"
													></div>
													<span class="text-purple-600 font-semibold tracking-wide">In class</span>
												</div>
												<div
													class="col-span-1 sm:col-span-2 h-24 bg-purple-300 border-2 border-dashed border-purple-600 rounded grid place-items-center"
												>
													<p class="font-extrabold text-purple-600 tracking-wide">
														Lecture (2 hours)
													</p>
												</div>
												<div
													class="col-span-1 sm:col-span-2 h-20 bg-purple-300 border-2 border-dashed border-purple-600 rounded grid place-items-center"
												>
													<p class="font-extrabold text-purple-600 tracking-wide">
														Pair Programming (2 hour)
													</p>
												</div>
												<div
													class="col-span-1 sm:col-span-2 h-12 bg-blue-300 border-2 border-dashed border-blue-600 rounded grid place-items-center"
												>
													<p class="font-extrabold text-blue-600 tracking-wide">
														Homework (1 hour)
													</p>
												</div>
											</div>
										</div>
									</div>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="pairprogram" data-scroll-spy="pairprogram">
							<div class="space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Programming Together
								</h2>
								<p class="text-lg">
									To get you ready for a career in coding. It is vital to work as part of a team.
									Cooperation is a key skill of any great programmer. At DevPioneer Institute you
									will be put on a small team of programmers to work on projects together.
								</p>

								<img
									class="max-w-full object-cover"
									src="/images/pairprogram.jpg"
									alt="A group of successful programmers working together"
								/>
								<h3 class="text-2xl font-semibold">
									Working together provides real-world experience
								</h3>
								<p class="text-lg">
									Employers are always looking for someone with industry experience. By working as
									part of a team at DevPioneer Institute you prepare yourself to work as part of a
									team of programmers in real-world environments.
								</p>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="careerprep" data-scroll-spy="careerprep">
							<div class="space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">
									Career Preparation
								</h2>
								<p>
									DevPioneer Institute offers career services for those who complete the part-time
									program. DevPioneer Institute provides the guidance and tools you need to blaze
									your trail and land the ideal web developer role for you.
								</p>
								<div class="grid grid-cols-12 gap-x-4 gap-y-8 lg:gap-6 items-start">
									<div class="col-span-12 lg:col-span-6 grid gap-2">
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
												d="M6 6.878V6a2.25 2.25 0 0 1 2.25-2.25h7.5A2.25 2.25 0 0 1 18 6v.878m-12 0c.235-.083.487-.128.75-.128h10.5c.263 0 .515.045.75.128m-12 0A2.25 2.25 0 0 0 4.5 9v.878m13.5-3A2.25 2.25 0 0 1 19.5 9v.878m0 0a2.246 2.246 0 0 0-.75-.128H5.25c-.263 0-.515.045-.75.128m15 0A2.25 2.25 0 0 1 21 12v6a2.25 2.25 0 0 1-2.25 2.25H5.25A2.25 2.25 0 0 1 3 18v-6c0-.98.626-1.813 1.5-2.122"
											/>
										</svg>
										<p class="font-semibold">Portfolio of Apps</p>
										<p>
											Throughout your journey at DevPioneer Institute you will complete projects
											that can demonstrate to employers your skills.
										</p>
									</div>
									<div class="col-span-12 lg:col-span-6 grid gap-2">
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
												d="M5.25 8.25h15m-16.5 7.5h15m-1.8-13.5-3.9 19.5m-2.1-19.5-3.9 19.5"
											/>
										</svg>
										<p class="font-semibold">Social Media Profiles</p>
										<p>
											You'll work with our career coaches to complete your LinkedIn and GitHub
											profiles to start the networking process.
										</p>
									</div>
									<div class="col-span-12 lg:col-span-6 grid gap-2">
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
												d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z"
											/>
										</svg>
										<p class="font-semibold">Resume</p>
										<p>
											An important aspect of the job hunt is having the perfect resume. You will
											work with our career coaches to polish your resume and become the perfect
											candidate for the job.
										</p>
									</div>
									<div class="col-span-12 lg:col-span-6 grid gap-2">
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
												d="M20.25 8.511c.884.284 1.5 1.128 1.5 2.097v4.286c0 1.136-.847 2.1-1.98 2.193-.34.027-.68.052-1.02.072v3.091l-3-3c-1.354 0-2.694-.055-4.02-.163a2.115 2.115 0 0 1-.825-.242m9.345-8.334a2.126 2.126 0 0 0-.476-.095 48.64 48.64 0 0 0-8.048 0c-1.131.094-1.976 1.057-1.976 2.192v4.286c0 .837.46 1.58 1.155 1.951m9.345-8.334V6.637c0-1.621-1.152-3.026-2.76-3.235A48.455 48.455 0 0 0 11.25 3c-2.115 0-4.198.137-6.24.402-1.608.209-2.76 1.614-2.76 3.235v6.226c0 1.621 1.152 3.026 2.76 3.235.577.075 1.157.14 1.74.194V21l4.155-4.155"
											/>
										</svg>
										<p class="font-semibold">Interview Prep</p>
										<p>
											DevPioneer Institute career advisors will hold mock interviews with you. To
											prepare you for technical and non-technical aspects of the interview process.
										</p>
									</div>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="admissions" data-scroll-spy="admissions">
							<div class="space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">Admissions</h2>
								<p>
									At DevPioneer Institute we want to understand what motivates you. The admissions
									process encourages you to share what your abilities and goals are so we can best
									help you on your journey. We want you to succeed with us at DevPioneer Institute.
								</p>
								<p>
									The Part-time program is an immersive journey. It was developed by our top
									DevPioneer Institute scientists to prepare you for a career in tech. Blazing your
									trail with the Part-time program allows you to keep your current job while you
									take evening classes.
								</p>
								<p>Prospective pioneers need to be:</p>
								<div class="grid grid-cols-12 gap-6 items-start">
									<div class="grid col-span-12 lg:col-span-4 gap-2">
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
										<p class="font-semibold">Commitment</p>
										<p>You need to be committed to learning the course material after work.</p>
									</div>
									<div class="grid col-span-12 lg:col-span-4 gap-2">
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
												d="M9 3.75H6.912a2.25 2.25 0 0 0-2.15 1.588L2.35 13.177a2.25 2.25 0 0 0-.1.661V18a2.25 2.25 0 0 0 2.25 2.25h15A2.25 2.25 0 0 0 21.75 18v-4.162c0-.224-.034-.447-.1-.661L19.24 5.338a2.25 2.25 0 0 0-2.15-1.588H15M2.25 13.5h3.86a2.25 2.25 0 0 1 2.012 1.244l.256.512a2.25 2.25 0 0 0 2.013 1.244h3.218a2.25 2.25 0 0 0 2.013-1.244l.256-.512a2.25 2.25 0 0 1 2.013-1.244h3.859M12 3v8.25m0 0-3-3m3 3 3-3"
											/>
										</svg>
										<p class="font-semibold">Dedication</p>
										<p>You need to be dedicated to completing your assignments.</p>
									</div>
									<div class="grid col-span-12 lg:col-span-4 gap-2">
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
												d="M2.25 18 9 11.25l4.306 4.306a11.95 11.95 0 0 1 5.814-5.518l2.74-1.22m0 0-5.94-2.281m5.94 2.28-2.28 5.941"
											/>
										</svg>
										<p class="font-semibold">Growth</p>
										<p>Always striving to learn more and continuing your technology journey.</p>
									</div>
								</div>
								<div class="pt-6">
									<a
										href="/admissions"
										class="inline-block py-2 px-4 bg-indigo-600 text-white text-base text-center font-medium rounded-md hover:bg-indigo-700/75 tracking-widest uppercase"
										>Start Your Application</a
									>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="testimonials" data-scroll-spy="testimonials">
							<div class="space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">Testimonials</h2>
								<div class="grid grid-cols-12 gap-x-4 gap-y-8 lg:gap-6">
									<div
										class="col-span-12 lg:col-span-6 p-6 border border-gray-200 shadow rounded-lg grid grid-rows-[1fr_auto]"
									>
										<p>
											A word of advice to older prospective students like myself. You may be
											frustrated where you are right now but afraid to make the leap, to quit your
											job, to spend your savings on a bootcamp, to take three months to learn, to
											work 80 hours a week. I promise it's worth it.
										</p>
										<div class="mt-6">
											<p>Andrew Ash</p>
											<p>Front-end Engineer</p>
										</div>
									</div>
									<div
										class="col-span-12 lg:col-span-6 p-6 border border-gray-200 shadow rounded-lg grid grid-rows-[1fr_auto]"
									>
										<p>
											DevPioneer Institute is, by all measures, the best investment I have made to
											date, and I would wholeheartedly recommend it to anybody considering it,
											especially those with little to no prior programming knowledge. I will note,
											however, that hard, consistent, and dedicated individual work is a must if you
											want to make the most out of the DevPioneer Institute investment.
										</p>
										<div class="mt-6">
											<p>Sally Smerna</p>
											<p>Front-end Engineer</p>
										</div>
									</div>
									<div
										class="col-span-12 lg:col-span-6 p-6 border border-gray-200 shadow rounded-lg grid grid-rows-[1fr_auto]"
									>
										<p>
											The instructors are always available for one-on-one help and will take the
											time to guide you through questions and problems. Their level of engagement in
											each student's learning process is what sets DevPioneer Institute apart.
										</p>
										<div class="mt-6">
											<p>Lisa Miner</p>
											<p>Front-end Engineer</p>
										</div>
									</div>
									<div
										class="col-span-12 lg:col-span-6 p-6 border border-gray-200 shadow rounded-lg grid grid-rows-[1fr_auto]"
									>
										<p>
											Within 4 weeks, I received 2 job offers at companies I was really excited
											about. During my interviews, both companies were pleasantly surprised by how
											knowledgeable and capable a bootcamp grad could be. Truly, I owe it all to
											DevPioneer Institute's education and preparation.
										</p>
										<div class="mt-6">
											<p>Benny Jetts</p>
											<p>Front-end Engineer</p>
										</div>
									</div>
								</div>
							</div>
						</div>
						<hr class="border-0 h-px bg-gray-200 my-6" />
						<div class="py-16" id="faqs" data-scroll-spy="faqs">
							<div class="space-y-6">
								<h2 class="text-3xl sm:text-4xl text-indigo-700 font-extrabold">FAQs</h2>
								<ul class="space-y-6">
									{#each questions as { question, answer }}
										<Accordion {question} {answer} />
									{/each}
								</ul>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</main>
