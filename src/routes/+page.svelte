<script>
	import Logo from '$lib/icons/Logo.svelte'
	let stickers = import.meta.glob("/static/stickers/*.svg", { eager: true });

</script>

<Logo />

<h1 class="font-bold text-2xl mb-4">Stickers</h1>

<div class="grid grid-cols-2 xl:grid-cols-3 gap-2 xl:gap-4">
	{#each Object.keys(stickers) as sticker}
		<img src={sticker.replace("/static", "")} class="rounded xl:rounded-lg"/>
	{/each}
</div>