<script lang="ts">
  import whiteLogo from "$lib/images/logos/whiteLogoSlim.png";
  import whiteIcon from "$lib/images/icons/whiteIcon.png";
  import Dropdown from "./Dropdown.svelte";
  import Menu from "./icons/Menu.svelte";
  import Exit from "./icons/Exit.svelte";

  let links = [
    { title: "Pricing", link: "/pricing" },
    { title: "About", link: "/about" },
    { title: "Contact Us", link: "/contact" },
  ];

  let outerWidth: number;

  let isDropdown: boolean = false;

  function handleDropdown() {
    isDropdown = !isDropdown;
  }

  function handleDocumentClick(event: MouseEvent) {
    if (isDropdown) {
      const target = event.target as HTMLElement;
      const dropdown = document.querySelector(".dropdown");
      if (
        !dropdown?.contains(target) &&
        !target.classList.contains("menu-btn") &&
        !target.classList.contains("drop-link")
      )
        isDropdown = false;
    }
  }

  $: if (outerWidth > 500) {
    isDropdown = false;
  }
</script>

<svelte:window bind:outerWidth />
<svelte:document on:click={handleDocumentClick}/>

<nav>
  <div class="nav-item-container">
    <a href="/">
      {#if outerWidth > 750}
        <img class="logo" src={whiteLogo} alt="Bright Wick Productions" />
      {:else}
        <img class="icon" src={whiteIcon} alt="Bright Wick Logo" />
      {/if}
    </a>
  </div>
  <div class="nav-item-container">
    {#if outerWidth > 500}
      {#each links as link}
        <a href={link.link} class:contact={link.title === "Contact Us"}
          >{link.title}</a
        >
      {/each}
    {:else}
      <button class="dropdown-btn" on:click={handleDropdown}>
        {#if !isDropdown}
          <Menu />
        {:else}
          <Exit />
        {/if}
      </button>
      {#if isDropdown}
        <Dropdown>
          {#each links as link}
            <a href={link.link} class="dropdown-link" on:click={handleDropdown}>{link.title}</a>
          {/each}
        </Dropdown>
      {/if}
    {/if}
  </div>
</nav>

<div></div>

<style>
  nav {
    position: relative;
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

  .icon {
    max-width: 100px;
    height: auto;
  }

  .dropdown-btn {
    background-color: transparent;
    border: none;
  }

  .dropdown-link {
    text-wrap: nowrap;
    color: white;
    text-decoration: none;
    padding: 0.5em;
    padding-left: 1em;
    border-bottom: 2px solid var(--brightwick-red);
  }
  @media (max-width: 750px) {
    nav {
      margin: 0 1em 0 1em;
    }
  }
</style>
