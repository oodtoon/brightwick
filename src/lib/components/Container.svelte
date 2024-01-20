<script lang="ts">
  export let isExamples = false 
</script>


<div class="container" class:isExamples>
  <slot />
</div>

<style>
  .container {
    margin: 2em;
    display: flex;
    flex-direction: column;
    gap: 2em;
  }

  .isExamples {
    gap: 5em
  }

  @media (max-width: 500px) {
    .container {
      margin: 1em;
    }
  }

  @media (max-width: 280px) {
    .container {
      margin: .5em;
    }
  }
</style>
