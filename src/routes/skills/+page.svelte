<script>
	import Skill from '../../components/skill/Skill.svelte';
	import ExperienceCard from '../../components/experienceCard/ExperienceCard.svelte';
	const skills = ['JavaScript', 'React', 'Front-end'];
	const experiences = [
		{
			jobTitle: 'Frontend Developer',
			company: 'ConcertAI',
			tenure: '2021 - present',
			jobDescription:
				'The Clinical AI & RWD Leader specialising to improve outcomes for patients through real world data and AI technologies.'
		}
	];
</script>

<main class="main">
	<div class="grid grid-cols-2">
		<div><h1 class="text-4xl my-2">Skill & Experience</h1></div>
		<div>
			{#each skills as skill}
				<Skill skillTitle={skill} />
			{/each}
			<div class="experiencesWrapper">
				{#each experiences as experience}
					<ExperienceCard
						jobTitle={experience.jobTitle}
						company={experience.company}
						tenure={experience.tenure}
						jobDescription={experience.jobDescription}
					/>
				{/each}
			</div>
		</div>
	</div>
</main>

<style>
	.main {
		color: #fff;
		margin-top: 8vh;
		margin-left: 15vw;
		font-family: roboto-regular;
	}
	.experiencesWrapper {
		margin-top: 8vh;
		padding: 16px 16px 16px 0;
	}
</style>
