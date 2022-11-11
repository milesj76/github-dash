<script>
    import DiGithubBadge from 'svelte-icons/di/DiGithubBadge.svelte'
    import FaRegBell from 'svelte-icons/fa/FaRegBell.svelte'
    import GoPlusSmall from 'svelte-icons/go/GoPlusSmall.svelte'
    import IoMdArrowDropdown from 'svelte-icons/io/IoMdArrowDropdown.svelte'
    import FaUser from 'svelte-icons/fa/FaUser.svelte'
    
</script>

<nav class="max-h-14 flex items-center bg-gray-800 px-3 py-2 text-white">
    <div class="h-11">
        <DiGithubBadge />
    </div>
    <form class="flex px-1 py-1 border rounded-md border-gray-600 text-sm max-w-4xl">
        <input type="text" placeholder="Search or jump to..."
        class="ml-2 bg-gray-800 grow">
        <button class="text-xs text-gray-400 h-5 w-5 p-0 border border-gray-500 bg-gray-800 rounded-md hover:transition-none">/</button>
    </form>
    <ul class="inline-flex gap-3 grow-0 mx-4 text-md">
        <li><a href="#">Pulls</a></li>
        <li><a href="#">Issues</a></li>
        <li><a href="#">Marketplace</a></li>
        <li><a href="#">Explore</a></li>
    </ul>
    <ul class="flex-end inline-flex gap-3 grow-0 ml-auto">
        <li class="h-5"><FaRegBell /></li>
        <li class="h-5 inline-flex"><GoPlusSmall /><IoMdArrowDropdown /></li>
        <li class="h-5 inline-flex"><FaUser /><IoMdArrowDropdown /></li>
    </ul>
</nav>