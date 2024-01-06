<script>
  import "../app.css";
  import Nav from "$lib/components/Nav.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<main>
  <Nav />
  <slot />
</main>
<Footer />

<style>
  main {
    min-height: calc(100vh - 60px);
  }
</style>
