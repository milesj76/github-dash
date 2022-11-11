<script>
  import Nav from "./components/Nav.svelte";
  import MainContent from "./components/MainContent.svelte";
  import Sidebar from "./components/Sidebar.svelte";

</script>

<main class="relative top-0 min-h-screen bg-white">
  <Nav />

  <!-- Add Sidebar & Content -->
  <div class="grid all-contents min-h-screen text-black">
    <aside class="sticky top-0 max-h-screen border-r border-gray-300">
      <Sidebar />
    </aside>

    <div class="text-center">
      <MainContent />
      
      <footer class="w-full bg-slate-100 text-slate-600">
        <ul class="grid grid-rows-3 grid-cols-3 px-6 pb-6 text-left text-[12px]">
          <li>Blog</li>
          <li>API</li>
          <li>Terms</li>
          <li>About</li>
          <li>Training</li>
          <li>Privacy</li>
          <li>Shop</li>
          <li>Status</li>
          <li>Docs</li>
          <li>Contact GitHub</li>
          <li>Security</li>
          <li>Pricing</li>
        </ul>
      </footer>
    </div>
  </div>

  <!-- Bottom border -->
  <div class="border-t h-1 border-gray-300">
    <br />
  </div>
</main>

<style>
  .all-contents {
    grid-template-columns: 18rem 1fr;
  }
</style>
