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
      <a href="/">
        <img class="logo" src={whiteLogo} alt="Bright Wick Productions" />
      </a>
      <div class="socials-container">
        <a href="www.youtube.com">
          <YouTube />
        </a>
        <a href="www.instagram.com">
          <Insta />
        </a>
        <a href="www.twitch.com">
          <Twitch />
        </a>
      </div>
    </div>
    <div class="links-container">
      <a href="/pricing">Pricing</a>
      <a href="/about">About</a>
      <a href="/contact">Contact Us</a>
    </div>
  </div>
  <div class="rights">
    All rights reserved {date.getFullYear()}
  </div>
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

  .rights {
    color: var(--brightwick-red)
  }

  @media (max-width: 350px) {
    .footer-content-container {
      flex-direction: column;
    }

    .links-container {
      margin: auto;
    }
  }
</style>
