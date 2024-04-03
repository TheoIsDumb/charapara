<script>
	let stickers = import.meta.glob("/src/stickers/*.svg", { eager: true });
	let designs = import.meta.glob("/src/designs/*.svg", { eager: true });

	const h1class = "my-4 text-4xl text-blue-400"
</script>

<h1 class={h1class}>സ്റ്റിക്കറുകൾ</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4 mb-4">
	{#each Object.keys(stickers) as sticker}
		<img src={sticker} alt="img: {sticker}" class="rounded xl:rounded-lg aspect-square object-cover h-full w-full"/>
	{/each}
</div>

<h1 class={h1class}>വരപ്പ്</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4 mb-4">
	{#each Object.keys(designs) as design}
		<img src={design} alt="img: {design}" class="rounded xl:rounded-lg aspect-square object-cover h-full w-full"/>
	{/each}
</div>