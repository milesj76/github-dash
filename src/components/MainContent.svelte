<script>
    import MdCode from 'svelte-icons/md/MdCode.svelte'
    import MdMoreHoriz from 'svelte-icons/md/MdMoreHoriz.svelte'
    import FaLock from 'svelte-icons/fa/FaLock.svelte'
    import TiBook from 'svelte-icons/ti/TiBook.svelte'

    import ContentCard from './ContentCard.svelte';

    const handleNewRepo = () => {}

    const genericContent = [
        {
            id: 0,
            title: "Generic 1",
            desc: "This is some generic content",
            content: "This is the most comprehensive version of the Kevin Bacon game on the web. The object of the game is to start with any actor or actress who has been in a movie and connect them to Kevin Bacon in the smallest number of links possible. Two people are linked if they've been in a movie together. We do not consider links through television shows, made-for-tv movies, writers, producers, directors, etc."
        },
        {
            id: 1,
            title: "Deez",
            desc: "Keepin it mad generic",
            content: "Then we can count how many links were necessary and assign the actor or actress a Bacon number. Bacon numbers higher than 4 are very rare. In the example above, Mary Pickford has a Bacon number of 3. The Oracle uses the data from Wikipedia and can give you the shortest path from every actor and actress that can be connected to Kevin Bacon."
        },
        {
            id: 2,
            title: "Wowzers Batman!",
            desc: "Sometimes we do a little memery...",
            content: "Every couple of weeks the Oracle downloads every English-language article from Wikipedia. Using an open-source script, we produce a JSON file with 128,000 films and 358,000 actors and actresses. There is a database service running at all times that stores the database file in memory. It is written in C for maximum CPU and memory efficiency. The service handles three different types of requests:"
        },
        {
            id: 3,
            title: "Gee whilackers!",
            desc: "You won't believe what you see next!",
            content: "There are several PHP pages -- one for each of the above types of queries -- that run on the Oracle of Bacon web server, which all connect to the database service using TCP. The database service uses a breadth-first search (BFS) to find the shortest path between pairs of actors. If you want to dig further into how shortest-path algorithms work, I recommend the textbook by Cormen, Leiserson, Rivest, and Stein as an excellent place to start. Other algorithms textbooks are likely to cover the subject as well, if Introduction to Algorithms isn't available. You may also look at materials that I wrote to explain graph algorithms (including BFS) to Duke undergraduate CS students here."
        },
    ]
</script>

<section class="w-full bg-slate-100 py-8 px-4 text-slate-800 leading-8">
    <header>
        <h1 class="text-4xl font-semibold text-left py-2">The home for all developers — including you.</h1>
        <p class="py-2 text-sm text-left text-gray-600">Welcome to your personal dashboard, where you can find an introduction to how GitHub works, tools to help you build software, and help merging your first lines of code.</p>
        <div class="inline-flex w-full mt-6 py-2">
            <div class="inline-flex h-8 w-8 p-[0.31rem] mr-1 bg-slate-300 rounded-full text-gray-500"><MdCode /></div>
            <span class="w-full p-1 text-left text-sm text-gray-600">Start writing code</span>
            <div class="h-8 w-8 p-1 text-gray-600"><MdMoreHoriz /></div>
        </div>
    </header>

    <article class="p-4 my-2 bg-white border border-gray-300 rounded-md text-left shadow-md">
        <header>
            <h2 class="font-medium mb-2">Start a new repository</h2>
            <p class="text-sm text-left text-gray-600">A repository contains all of your project's files, revision history, and collaborator discussion.</p>
        </header>
        <form
            class="py-2"
            on:submit|preventDefault={handleNewRepo}>
            <div class="w-full flex items-center">
                <label class="mr-2 whitespace-nowrap" for="repoName">user /</label>
                <input
                    class="w-full px-4 py-1 bg-white text-sm placeholder:text-gray-600 border border-gray-300 rounded-md"
                    type="text" placeholder="name your new repository...">
            </div>
            <div class="inline-flex items-center text-gray-600">
                <input class="bg-red-400"
                    type="radio" name="repo-type" id="public">
                <div class="h-7 w-7 mx-2"><TiBook /></div>
                <div class="text-xs py-2">
                    <label class="font-semibold" for="public">Public</label>
                    <p class="text-gray-500">Anyone on the internet can see this repository</p>
                </div>
            </div>
            <div class="inline-flex items-center text-gray-600">
                <input class="bg-red-400"
                    type="radio" name="repo-type" id="private">
                <div class="h-7 w-7 mx-2"><FaLock /></div>
                <div class="text-xs py-2">
                    <label class="font-semibold" for="private">Private</label>
                    <p class="text-gray-500">You choose who can see and commit to this repository</p>
                </div>
            </div>
            <button class="flex py-[0.4rem] px-3 bg-green-600 hover:bg-green-700 border-green-700 hover:border-green-800 rounded-md text-white font-semibold text-xs"
                on:click={handleNewRepo}>Create a new repository</button>
        </form>
    </article>

    <article class="p-4 my-2 bg-white border border-gray-300 rounded-md text-left shadow-md">
        <header class="mb-4">
            <h2 class="font-medium mb-2">Introduce yourself with a profile README</h2>
            <p class="text-sm text-left text-gray-600">Share information about yourself by creating a profile README, which appears at the top of your profile page.</p>
        </header>
        <section class="border rounded-md border-gray-300">
            <div class="flex items-center px-4 py-2 border-b">
                <p class="w-full font-mono text-sm">user/README.md</p>
                <button class="flex py-[0.4rem] px-3 bg-green-600 hover:bg-green-700 border-green-700 hover:border-green-800 rounded-md text-white font-semibold text-xs">Create</button>
            </div>
            <ul class="font-mono py-2 px-4 text-sm bg-slate-100">
                <li>1 - 👋 Hi, I'm @user</li>
                <li>2 - 👀 I’m interested in ...</li>
                <li>3 - 🌱 I’m currently learning ...</li>
                <li>4 - 💞️ I’m looking to collaborate on ...</li>
                <li>5 - 📫 How to reach me ...</li>
                <li>6 </li>
            </ul>
        </section>
    </article>

    {#each genericContent as card}
        <ContentCard {card} />
    {/each}
</section>

<!-- The radio buttons can't be controlled very much without the @tailwind-forms plugin -->