<script>
	import { goto } from '$app/navigation';
	import Button from '../components/button/Button.svelte';
</script>

<main class="main">
	<h1 class="text-4xl my-2">Hi my name is</h1>
	<h2 class="text-[#64ffda] text-7xl my-2">Ayush Porwal</h2>
	<h2 class="text-4xl my-2">I am a software engineer at ConcertAI</h2>
	<Button buttonTitle="Contact Me" handleOnClick={() => goto('/contact')} />
</main>

<style>
	.main {
		color: #fff;
		margin-top: 15%;
		margin-left: 15%;
		font-family: roboto-regular;
	}
</style>
