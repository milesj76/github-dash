<script>
    export let card
    let { title, desc, content } = card 

</script>

<article class="p-4 my-2 bg-white border border-gray-300 rounded-md text-left shadow-md">
    <header class="mb-4">
        <h2 class="font-medium mb-2">{title}</h2>
        <p class="text-sm text-left text-gray-600">{desc}</p>
    </header>
    <section class="py-4 px-6 leading-7 text-gray-700 border rounded-md border-gray-300 bg-slate-100">
        <p>{content}</p>
    </section>
</article>