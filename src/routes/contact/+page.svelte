<script lang="ts">
  import Title from "$lib/components/Title.svelte";
  import Container from "$lib/components/Container.svelte";
</script>

<Container>
  <Title title={"Schedule a Call With Us!"} />

  <iframe
    class="calendar"
    title="Schedule A Call With Us!"
    src="https://calendar.google.com/calendar/u/0/appointments/schedules/AcZssZ28xZKwYu9zkxJxkHjQvFOIJ2AbTzuGW0KRVmsX3z5hdbveozoHLMXcDJUIAcCTos0FdtxXGcDK?pli=1"
  ></iframe>
</Container>

<style>
  .calendar {
    width: 90%;
    min-height: 800px;
    margin: auto;
  }
</style>
