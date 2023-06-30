<script lang="ts">
	import Icon from '@iconify/svelte';
	import Avatar from '../Avatar.svelte';
	import MenuItem from './MenuItem.svelte';

	let isOpen = false;

	const toggleOpen = () => (isOpen = !isOpen);
</script>

<div class="nav-right">
	<div class="wrapper">
		<button class="host-cta" on:click={() => {}}>Airbnb your home </button>
		<button class="nav-dropdown-btn" on:click={toggleOpen}
			><Icon icon="ant-design:menu-outlined" />
			<div class="avatar-wrapper">
				<Avatar />
			</div>
		</button>
	</div>
	{#if isOpen}
		<div class="nav-dropdown-menu-wrapper">
			<div class="nav-dropdown-menu">
				<MenuItem onClick={() => {}} label="Login" />
				<MenuItem onClick={() => {}} label="Sign up" />
			</div>
		</div>
	{/if}
</div>

<style lang="postcss">
	.nav-right {
		@apply relative;
	}
	.wrapper {
		@apply flex flex-row items-center gap-3;
	}
	.host-cta {
		@apply hidden md:block text-sm font-semibold py-3 px-4 rounded-full hover:bg-neutral-100 transition cursor-pointer;
	}
	.nav-dropdown-btn {
		@apply p-4 md:py-1 md:px-2 border-[1px] border-neutral-200 flex flex-row items-center gap-3 rounded-full cursor-pointer hover:shadow-md transition;
	}
	.avatar-wrapper {
		@apply hidden md:block;
	}
	.nav-dropdown-menu-wrapper {
		@apply absolute rounded-xl shadow-md w-[40vw] md:w-3/4 bg-white overflow-hidden right-0 top-12 text-sm;
	}
	.nav-dropdown-menu {
		@apply flex flex-col cursor-pointer;
	}
</style>
