<script lang="ts">
  import WhiteWick from "$lib/components/icons/WhiteWick.svelte";
  import whiteLogo from "$lib/images/logos/whiteLogoSlim.png"
</script>

<nav>
  <div class="nav-item-container">
    <a href="/">
      <img class="logo" src={whiteLogo} alt="Bright Wick Productions"/>
    </a>
  </div>
  <div class="nav-item-container">
    <a href="/pricing">Pricing</a>
    <a href="/">About</a>
    <a href="/">Story</a>
    <a class="contact" href="/">Contact Us</a>
  </div>
</nav>

<div></div>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    margin: 0 5em 0 5em;
    padding: 1em;
  }

  .nav-item-container {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    gap: 3em;
  }

  .contact {
    color: white;
    background-color: var(--brightwick-red);
    border: 3px solid white;
    padding: 1em 2em;
    border-radius: 40px;
  }

  .contact:hover {
    background-color: transparent;
    border-color: var(--brightwick-red);
  }

  .logo {
    max-width: 200px;
    height: auto;
  }
</style>
