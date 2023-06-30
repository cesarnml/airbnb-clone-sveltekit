<script lang="ts">
	import Container from '$/components/Container.svelte';
	import Logo from './Logo.svelte';
	import Search from './Search.svelte';
	import UserMenu from './UserMenu.svelte';
</script>

<div class="nav">
	<div class="inner-nav">
		<Container>
			<div class="logo-wrapper">
				<Logo />
				<Search />
				<UserMenu />
			</div>
		</Container>
	</div>
</div>

<style lang="postcss">
	.nav {
		@apply fixed w-full bg-white z-10 shadow-sm;
	}
	.inner-nav {
		@apply py-4 border-b-[1px];
	}
	.logo-wrapper {
		@apply flex flex-row items-center justify-between gap-3 md:gap-0;
	}
</style>
