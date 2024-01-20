<script lang="ts">
  export let name: string;
  export let paragraphs: string[];
</script>

<div class="partner-container">
  <h2 class="name">{name}</h2>
  {#each paragraphs as paragraph}
    <p>{paragraph}</p>
  {/each}
</div>

<style>
  .partner-container {
    max-width: 800px;
    margin: auto;
  }

  .name {
    text-decoration: underline solid var(--brightwick-red);
  }
</style>
