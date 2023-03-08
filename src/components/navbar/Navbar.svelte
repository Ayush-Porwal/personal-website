<script>
	import { page } from '$app/stores';
	import { goto } from '$app/navigation';
	const navItems = ['Home', 'Skills', 'Blogs', 'Contact', 'Resume'];
</script>

<nav class="w-screen h-[60px] text-white cursor-pointer bg-[#222639] shadow-xl flex justify-between">
	<!-- svelte-ignore a11y-click-events-have-key-events -->
	<div
		class="ml-[24px] hover:text-[#64ffda] icon-home flex items-center text-5xl"
		on:click={() => {
			goto('/');
		}}
	/>
	<div class="flex mr-[24px] gap-4 md:gap-8 lg:gap-8">
		{#each navItems as item}
			<a
				href={`/${item === 'Home' ? '' : item.toLowerCase()}`}
				class={`${
					$page.url.pathname.slice(1) === (item === 'Home' ? '' : item.toLowerCase())
						? 'active-tab'
						: ''
				} items flex items-center justify-center`}
			>
				{item}
			</a>
		{/each}
	</div>
</nav>

<style lang="scss">
	.items {
		font-size: 24px;
		font-family: roboto-bold;
		cursor: pointer;
		&:hover {
			color: #64ffda;
		}
	}
	.active-tab {
		color: #64ffda;
	}
</style>
