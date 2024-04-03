<script>
    import Logo from '$lib/icons/Logo.svelte'
    import Github from '$lib/icons/Github.svelte'
</script>

<header class="relative">
    <div class="h-60 bg-[#232a2d] w-full flex flex-col justify-center items-center" />

    <img src="/curve.svg" alt="te" class="w-full h-fit"/>


    <div class="absolute flex h-60 flex-col gap-4 justify-center items-center left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 w-dvw">
        <Logo/>

        <span class="text-3xl text-blue-400 text-center">
            മലയാളി ഡെവ് സ്റ്റിക്കറുകൾ!
        </span>

        <a class="text-xl bg-gradient-to-b from-blue-500 to-blue-400 text-white shadow rounded py-2 px-8 not-italic" href="#">
            <Github />
        </a>
    </div>
</header>