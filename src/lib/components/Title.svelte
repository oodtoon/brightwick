<script lang="ts">
  export let title: string;
</script>

<div class="title-container">
  <h1 class="title">{title}</h1>
</div>

<style>
  .title-container {
    margin: auto;
  }

  .title {
    text-decoration: underline solid var(--brightwick-red);
  }
</style>
