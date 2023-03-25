<script>
	export let email = 'xyz@abcmail.com';
</script>

<div class="w-full fixed bottom-0 py-4 bg-[#222639]">
	<div class="flex justify-center gap-4 items-center">
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<div
			class="icon-github text-white text-xl hover:text-[#64FFDA] cursor-pointer"
			on:click={() => {
				window.open('https://github.com/porwal-ayush', '_blank');
			}}
		/>
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<div
			class="icon-linkedin text-white text-xl hover:text-[#64FFDA] cursor-pointer"
			on:click={() => {
				window.open('https://www.linkedin.com/in/ayush-porwal/', '_blank');
			}}
		/>
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<div
			class="icon-instagram text-white text-xl hover:text-[#64FFDA] cursor-pointer"
			on:click={() => {
				window.open('https://www.instagram.com/prom_cooks/', '_blank');
			}}
		/>
		<div class="text-white text-sm hover:text-[#64FFDA]">{email}</div>
	</div>
</div>
