<script>
    import FaUser from "svelte-icons/fa/FaUser.svelte";
    import IoMdArrowDropdown from "svelte-icons/io/IoMdArrowDropdown.svelte";
    import MdCollectionsBookmark from 'svelte-icons/md/MdCollectionsBookmark.svelte'

    const handleFindRepo = () => {}
    const handleFindTeams = () => {}

    let projects = [
        "user/learning-to-code",
        "user/project2",
        "tesla/fast-and-quiet",
        "atlantic/deep-sea-scuba",
        "user/nuclear-sub-hacks",
        "mattress/not-money-laundering",
    ]
    
    let teams = [
        "chingu-coders/team-gold",
        "github/data-managers",
        "microsoft/big-boys-of-bill-gates",
    ]
</script>

<section class="py-6 px-6">
    <header class="border-b border-gray-400 py-4 pt-2">
        <div class="h-5 inline-flex text-sm gap-1">
            <FaUser />
            User123
            <IoMdArrowDropdown /></div>
    </header>

    <!-- Recent Repositories -->
    <article class="py-4">
        <div class="flex justify-between align-middle py-2">
            <h2 class="font-medium">Recent Repositories</h2>
            <button class="flex py-[0.4rem] px-3 bg-green-600 hover:bg-green-700 border-green-700 hover:border-green-800 rounded-md text-white font-normal text-xs">
                <div class="h-4 mr-1">
                    <MdCollectionsBookmark />
                </div>
                <p>New</p>
            </button>
        </div>

        <form
            class="pb-2"
            on:submit|preventDefault={handleFindRepo}>
            <input
            class="w-full py-1 px-2 text-sm border border-slate-300 rounded-md bg-slate-100"
            type="text"
            placeholder="Find a repository...">
        </form>

        <ul class="py-2">
            {#each projects as project}
                <li class="text-[14px] font-extralight">
                    <a class="text-gray-600 hover:underline hover:text-gray-900" 
                    href="#">{project}</a>
                </li>
            {/each}
        </ul>

        <div>
            <button class="w-full text-left text-xs p-0 bg-white text-gray-400 hover:text-blue-400"
            >Show more</button>
        </div>
    </article>

    <!-- Recent activity -->
    <article class="mb-4">
        <div class="py-2">
            <h2 class="font-semibold">Recent activity</h2>
        </div>
        <div class="w-full py-4 px-4 border border-slate-300 border-dashed rounded-lg text-xs text-slate-600">
            <p>When you take actions across GitHub, we'll provide links to that activity here.</p>
        </div>
    </article>

    <!-- Your teams -->
    <article>
        <div class="py-2">
            <h2 class="font-semibold">Your teams</h2>
        </div>

        <form
            class="pb-2"
            on:submit|preventDefault={handleFindTeams}>
            <input
            class="w-full py-1 px-2 text-sm border border-slate-300 rounded-md bg-slate-100"
            type="text"
            placeholder="Find a team...">
        </form>

        <ul class="py-2">
            {#each teams as team}
                <li class="text-[14px] font-extralight">
                    <a class="text-gray-600 hover:underline hover:text-gray-900" 
                    href="#">{team}</a>
                </li>
            {/each}
        </ul>
    </article>
</section>
