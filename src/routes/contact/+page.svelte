<script>
	import Button from '../../components/button/Button.svelte';
</script>

<main class="container mt-[15%] ml-[15%]">
	<div class="text-7xl my-2 text-[#64ffda]">Give me an opportunity</div>
	<div class="text-2xl text-white max-w-[70%] my-4 lg:my-10">
		I’m interested to work in ambitious and large projects. However, if you have other request or
		question, please don’t hesitate to contact.
	</div>
	<form class="flex flex-wrap gap-2 max-w-[70%]">
		<fieldset class="flex w-full gap-2">
			<input
				type="text"
				placeholder="Name"
				class="p-4 bg-[rgba(100,255,218,0.1)] w-1/2 rounded text-white"
			/>
			<input
				type="email"
				placeholder="Email"
				class="p-4 bg-[rgba(100,255,218,0.1)] w-1/2 rounded text-white"
			/>
		</fieldset>
		<input
			type="text"
			placeholder="Subject"
			class="p-4 bg-[rgba(100,255,218,0.1)] w-full rounded text-white"
		/>
		<textarea
			placeholder="Message"
			class="p-4 bg-[rgba(100,255,218,0.1)] w-full rounded text-white"
		/>
		<div class="flex justify-end w-full"><Button buttonTitle="Send Message!" /></div>
	</form>
</main>

<style>
	.container {
		font-family: roboto-regular;
	}
</style>
