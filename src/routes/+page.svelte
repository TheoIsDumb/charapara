<script>
	import Logo from '$lib/icons/Logo.svelte'
	let stickers = import.meta.glob("/src/stickers/*.svg", { eager: true });
	let designs = import.meta.glob("/src/designs/*.svg", { eager: true });

	let selected = stickers
</script>

<Logo />

<div class="w-full flex justify-between mb-2 text-5xl">
	<button on:click={() => selected = stickers}>Stickers</button>
	<button on:click={() => selected = designs}>designs</button>
</div>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4">
	{#each Object.keys(selected) as sticker}
		<img src={sticker} alt="img: {sticker}" class="rounded xl:rounded-lg aspect-square object-cover h-full w-full"/>
	{/each}
</div>