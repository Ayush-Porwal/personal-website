<script>
	import { page } from '$app/stores';
	import { goto } from '$app/navigation';
	const navItems = ['Home', 'Skills', 'Blogs', 'Contact', 'Resume'];
</script>

<nav class="navbar grid gap-64 grid-cols-2">
	<div
		class="icon icon-home flex items-center text-5xl"
		on:click={() => {
			goto('/');
		}}
	/>
	<div class="grid grid-cols-5">
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
	.navbar {
		width: 100vw;
		height: 60px;
		color: #fff;
		cursor: pointer;
		background-color: #222639;
		box-shadow: 0px 3px 4px rgba(0, 0, 0, 0.25);
	}

	.icon {
		margin-left: 24px;
		&:hover {
			color: #64ffda;
		}
	}

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
