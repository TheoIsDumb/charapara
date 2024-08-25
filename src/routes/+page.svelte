<script>
	let stickers = import.meta.glob("/static/stickers/*.svg", { eager: true });
	let designs = import.meta.glob("/static/designs/*.svg", { eager: true });

	const h1class = "py-4 text-4xl text-blue-400"
	const svgClass = "rounded xl:rounded-lg aspect-square h-full w-full"
</script>

<h1 class={h1class}>സ്റ്റിക്കറുകൾ</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4">
	{#each Object.keys(stickers) as sticker}
		<img src={sticker.replace("/static", "")}
		alt="img: {sticker}" class="{svgClass} hover:-rotate-6 transition duration-300"/>
	{/each}
</div>

<h1 class={h1class}>സംഭാവന 🗿</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4">
	<div class="community">
		<img src="/python.svg" alt="python" class="{svgClass} hover:-rotate-6 transition duration-300"/>

		<p class="text-center">മെയ്ഡ് ബൈ <a href="https://linkedin.com/in/ajithyesss" class="underline text-blue-300" target="_blank">അജിത്തണ്ണൻ</a></p>
	</div>
</div>

<h1 class={h1class}>വരപ്പ്</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4">
	{#each Object.keys(designs) as design}
		<img src={design.replace("/static", "")}
		alt="img: {design}" class={svgClass}/>
	{/each}
</div>
