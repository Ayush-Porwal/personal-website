<script>
	export let jobTitle = '';
	export let company = '';
	export let tenure = '';
	export let jobDescription = '';
</script>

<div class="cardContainer">
	<div class="spaceMaker">{jobTitle}</div>
	<div class="spaceMaker">{company}</div>
	<div class="spaceMaker">{tenure}</div>
	<div class="spaceMaker">{jobDescription}</div>
</div>

<style lang="scss">
	.cardContainer {
		background-color: rgba(100, 255, 218, 0.1);
		padding: 12px;
		width: 50%;
	}
	.spaceMaker {
		margin-bottom: 5px;
	}
</style>
