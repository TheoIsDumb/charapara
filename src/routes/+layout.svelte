<script>
    import "../app.pcss"
	import Header from '$lib/components/Header.svelte'
</script>

<Header />

<div class="w-[90%] xl:w-[1000px] p-2 mx-auto h-full">
    <slot />
</div>