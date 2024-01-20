<script lang="ts">
</script>

<div class="dropdown">
  <slot />
</div>


<style>
  .dropdown {
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    top: 8em;
    left: 50%;
    transform: translateX(-50%);
    width: 100vw;
    z-index: 5;
    background-color: black;
  }
</style>