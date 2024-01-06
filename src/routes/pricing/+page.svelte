<script lang="ts">
  import Container from "$lib/components/Container.svelte";

  const services = [
    {
      title: "Podcast",
      offer: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatibus
      magnam deleniti facere quae quaerat quo velit eaque molestiae, sapiente
      numquam ea exercitationem saepe harum iusto repellendus iste deserunt hic
      consequuntur.`,
      rate: "$500/podcast",
    },
    {
      title: "Company Call",
      offer: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatibus
      magnam deleniti facere quae quaerat quo velit eaque molestiae, sapiente
      numquam ea exercitationem saepe harum iusto repellendus iste deserunt hic
      consequuntur.`,
      rate: "$1,000/call",
    },
    {
      title: "Custom Project",
      offer: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatibus
      magnam deleniti facere quae quaerat quo velit eaque molestiae, sapiente
      numquam ea exercitationem saepe harum iusto repellendus iste deserunt hic
      consequuntur.`,
      rate: "$2,000 minimum",
    },
  ];
</script>

<Container>
  <div class="title-container">
    <h1>Pricing</h1>
  </div>

  <div class="services-container">
    {#each services as service, i}
      <div class="service" class:right-border={i < services.length - 1}>
        <h2>{service.title}</h2>
        <ul>
          {#each services as service, i}
            <li>selling point {i}</li>
          {/each}
        </ul>
        <div class="rate">{service.rate}</div>
      </div>
    {/each}
  </div>

  <div class="contact-container">
    <a href="/contact" class="contact">Schedule Consultation</a>
  </div>
</Container>

<style>
  .title-container {
    margin: auto;
  }

  .services-container {
    display: flex;
    margin: auto;
    align-items: center;
    justify-content: center;
    width: 900px;
  }

  .service {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 1em 2em;
  }

  ul {
    padding-inline-start: 0px;
  }

  .rate {
    font-weight: 800;
    font-size: 28px;
  }

  .contact-container {
    margin: auto;
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

  .right-border {
    border-right: 2px solid white;
  }
</style>
