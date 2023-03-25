<script>
	import { goto } from '$app/navigation';
	import Button from '../components/button/Button.svelte';
	import Skill from '../components/skill/Skill.svelte';
	import ExperienceCard from '../components/experienceCard/ExperienceCard.svelte';

	const skills = [
		'JavaScript',
		'Typescript',
		'Node',
		'React',
		'Redux',
		'Webpack',
		'Html',
		'Css3',
		'Tailwind',
		'Material-UI',
		'Front End',
		'Agile Methodlogy'
	];

	const experiences = [
		{
			jobTitle: 'Software Engineer',
			company: 'ConcertAI',
			tenure: '2021 - present',
			jobDescription:
				'The Clinical AI & RWD Leader specialising to improve outcomes for patients through real world data and AI technologies.'
		}
	];
</script>

<main class="overflow-auto h-[calc(100vh_-_124px)]">
	<div class="h-[calc(100vh_-_124px)] flex flex-col justify-center mx-auto w-3/4">
		<h1 class="text-white text-2xl md:text-4xl my-2">Hi my name is</h1>
		<h2 class="text-[#64ffda] text-2xl md:text-7xl my-2">Ayush Porwal</h2>
		<h2 class="text-white text-2xl md:text-4xl my-2">
			I am a software engineer at ConcertAI, with skills
		</h2>

		<div class="flex flex-col md:items-center md:flex-row my-2">
			<!-- <div class="text-3xl text-[#66FFDA]">I am proficient in</div> -->
			<div class="flex flex-wrap flex-row gap-2 my-2 md:my-0">
				{#each skills as skill}
					<Skill skillTitle={skill} />
				{/each}
			</div>
		</div>

		<Button buttonTitle="Contact Me" handleOnClick={() => goto('/contact')} />
		<!-- <div class="flex flex-wrap">
			{#each experiences as experience}
				<ExperienceCard
					jobTitle={experience.jobTitle}
					company={experience.company}
					tenure={experience.tenure}
					jobDescription={experience.jobDescription}
				/>
			{/each}
		</div> -->
	</div>
</main>
