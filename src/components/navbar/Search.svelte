<script lang="ts">
	import Icon from '@iconify/svelte';
</script>

<div class="search-wrapper">
	<div class="search-inner">
		<div class="location">Anywhere</div>
		<div class="time">Any Week</div>
		<div class="guest-search-wrapper">
			<div class="guest">Add Guests</div>
			<div class="search">
				<Icon icon="bx:search" />
			</div>
		</div>
	</div>
</div>

<style lang="postcss">
	.search-wrapper {
		@apply border-[1px] w-full md:w-auto py-2 rounded-full shadow-sm hover:shadow-md transition cursor-pointer;
	}
	.search-inner {
		@apply flex flex-row items-center justify-between;
	}
	.location {
		@apply text-sm font-semibold px-6;
	}
	.time {
		@apply hidden sm:block text-sm font-semibold px-6 border-x-[1px] flex-1 text-center;
	}
	.guest-search-wrapper {
		@apply text-sm pl-6 pr-2 text-gray-600 flex flex-row items-center gap-3;
	}
	.guest {
		@apply hidden sm:block font-semibold;
	}
	.search {
		@apply p-2 bg-rose-500 rounded-full text-white;
	}
</style>
