<script lang="ts">
  import whiteLogo from "$lib/images/logos/whiteLogoSlim.png";
  import YouTube from "./icons/YouTube.svelte";
  import Insta from "./icons/Insta.svelte";
  import Twitch from "./icons/Twitch.svelte";

  const date = new Date();
</script>

<footer>
  <div class="footer-content-container">
    <div class="content">
      <img class="logo" src={whiteLogo} alt="Bright Wick Productions" />
      <div class="socials-container">
        <YouTube />
        <Insta />
        <Twitch />
      </div>
    </div>
    <div class="links-container">
      <a href="/">Pricing</a>
      <a href="/">About</a>
      <a href="/">Story</a>
      <a href="/">Contact Us</a>
    </div>
  </div>
  All rights reserved {date.getFullYear()}
</footer>

<style>
  footer {
    display: flex;
    flex-direction: column;
  }

  .footer-content-container {
    display: flex;
    margin: auto;
    gap: 2em;
    align-items: flex-start;
  }

  .content {
    display: flex;
    flex-direction: column;
    gap: 1em;
  }

  .socials-container {
    display: flex;
    gap: 1em;
    align-self: center;
  }

  .links-container {
    display: flex;
    flex-direction: column;
    gap: 1em;
  }

  .logo {
    max-width: 200px;
    max-height: 55.55px;
  }
</style>
