<script lang="ts">
	import Button from '../../components/button/Button.svelte';
	import { toast } from '@zerodevx/svelte-toast';

	const defaultValues = {
		fullName: '',
		email: '',
		subject: '',
		message: ''
	};

	let formData = { ...defaultValues };
</script>

<main class="flex flex-col justify-center min-h-[calc(100vh_-_124px)] overflow-auto w-3/4 mx-auto">
	<div class="my-2 text-[#64ffda] text-5xl md:text-7xl">Give me an opportunity</div>
	<span class="text-xl md:text-2xl text-white my-4 lg:my-10">
		I’m interested to work in ambitious and large projects. However, if you have other request or
		question, please don’t hesitate to contact.
	</span>
	<form
		class="flex flex-col gap-2"
		id="contact_form"
		on:submit|preventDefault={() => {
			formData = { ...defaultValues };
			toast.push('Havent implemented the backend functionality yet...', {
				duration: 5000,
				theme: {
					'--toastColor': '#fff',
					'--toastBackground': '#273b48',
					'--toastBarBackground': '#273b48'
				}
			});
		}}
	>
		<fieldset class="flex flex-col md:flex-row w-full gap-2">
			<input
				type="text"
				placeholder="Full Name"
				bind:value={formData.fullName}
				required={true}
				class="p-4 bg-[rgba(100,255,218,0.1)] w-full md:w-1/2 rounded text-white"
			/>
			<input
				type="email"
				placeholder="Email"
				bind:value={formData.email}
				required={true}
				class="p-4 bg-[rgba(100,255,218,0.1)] w-full md:w-1/2 rounded text-white"
			/>
		</fieldset>
		<input
			type="text"
			placeholder="Subject"
			bind:value={formData.subject}
			required={true}
			class="p-4 bg-[rgba(100,255,218,0.1)] w-full rounded text-white"
		/>
		<textarea
			placeholder="Message"
			bind:value={formData.message}
			required={true}
			class="p-4 bg-[rgba(100,255,218,0.1)] w-full rounded text-white"
		/>
		<div class="flex justify-end w-full">
			<Button buttonTitle="Send Message!" />
		</div>
	</form>
</main>

<style>
	:root {
		--toastContainerTop: 80px;
		--toastContainerRight: 16px;
	}
</style>
