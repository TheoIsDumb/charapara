<script>
	let stickers = import.meta.glob("/static/stickers/*.svg", { eager: true });
	let designs = import.meta.glob("/static/designs/*.svg", { eager: true });

	const h1class = "my-4 text-4xl text-blue-400"
	const svgClass = "rounded xl:rounded-lg aspect-square object-cover h-full w-full hover:rotate-12 transition duration-300"
</script>

<h1 class={h1class}>സ്റ്റിക്കറുകൾ</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4 mb-4">
	{#each Object.keys(stickers) as sticker}
		<img src={sticker.replace("/static", "")}
		alt="img: {sticker}" class={svgClass}/>
	{/each}
</div>

<h1 class={h1class}>വരപ്പ്</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4 mb-4">
	{#each Object.keys(designs) as design}
		<img src={design.replace("/static", "")}
		alt="img: {design}" class={svgClass}/>
	{/each}
</div>