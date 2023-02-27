<script>
	export let buttonTitle = '';
	export let handleOnClick = () => {};
</script>

<button class="button" on:click={handleOnClick}>{buttonTitle}</button>

<style lang="scss">
	.button {
		color: #fff;
		width: 200px;
		font-size: 24px;
		margin: 1% 0 0 0;
		padding: 6px 12px;
		border: 1px solid #64ffda;
		background-color: transparent;
	}
</style>
