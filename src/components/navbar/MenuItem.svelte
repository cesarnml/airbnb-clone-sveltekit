<script lang="ts">
	export let onClick: () => void;
	export let label: string;
</script>

<button on:click={onClick}>{label}</button>

<style lang="postcss">
	button {
		@apply px-4 py-3 hover:bg-neutral-100 transition font-semibold;
	}
</style>
