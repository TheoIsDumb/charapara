<script>
	import Logo from '$lib/icons/Logo.svelte'
	let stickers = import.meta.glob("/src/stickers/*.svg", { eager: true });
	let designs = import.meta.glob("/src/designs/*.svg", { eager: true });

	const h1class = "my-4 font-bold text-4xl"
</script>

<Logo />

<h1 class={h1class}>Stickers</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4 mb-4">
	{#each Object.keys(stickers) as sticker}
		<img src={sticker} alt="img: {sticker}" class="rounded xl:rounded-lg aspect-square object-cover h-full w-full"/>
	{/each}
</div>

<h1 class={h1class}>Designs</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4 mb-4">
	{#each Object.keys(designs) as design}
		<img src={design} alt="img: {design}" class="rounded xl:rounded-lg aspect-square object-cover h-full w-full"/>
	{/each}
</div>