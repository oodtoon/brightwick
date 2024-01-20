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
</style>
