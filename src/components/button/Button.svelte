<script>
	export let buttonTitle = '';
	export let fullWidth = false;
	export let handleOnClick = () => {};
</script>

<button
	class={`text-white w-52 text-2xl px-[6px] py-[12px] m-[12px_0_0_0] border border-[#64ffda] bg-transparent ${
		fullWidth ? 'w-full' : ''
	}`}
	on:click={handleOnClick}>{buttonTitle}</button
>
