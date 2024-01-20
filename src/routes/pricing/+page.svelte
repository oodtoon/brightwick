<script lang="ts">
  import Container from "$lib/components/Container.svelte";
  import Title from "$lib/components/Title.svelte"

  const services = [
    {
      title: "Podcast",
      sellingPoints: [
        "1 Hour Podcast",
        "2 Pre-Cut Clips Per Person",
        "Fully Edited",
        "You Own the Rights",
      ],
      rate: "$500/podcast",
    },
    {
      title: "Company Call",
      sellingPoints: [
        "Live Steam",
        "Quick Connection",
        "High Quality Audio",
        "Keep a Recording",
      ],
      rate: "$1,000/call",
    },
    {
      title: "Custom Project",
      offer:
        "Need something more specific? We do customer projects to fit your needs. Please consultation and we'll discuss if we're right for you!",
      sellingPoints: ["You Own the Rights"],
      rate: "$2,000 minimum",
    },
  ];
</script>

<Container isExamples>
 <Title title={"Pricing"}/>

  <div class="services-container">
    {#each services as service}
      <div class="service alt-one">
        <h2>{service.title}</h2>
        {#if service.offer}
          <div>{service.offer}</div>
        {/if}
        <ul>
          {#each service.sellingPoints as point}
            <li>{point}</li>
          {/each}
        </ul>
        <div class="rate">{service.rate}</div>
      </div>
    {/each}
  </div>
  <div class="contact-container">
    <a href="/contact" class="contact alt-contact">Schedule Consultation</a>
  </div>
</Container>

<style>
  .services-container {
    display: flex;
    margin: auto;
    align-items: center;
    justify-content: center;
    width: 900px;
    gap: 2em;
  }

  .service {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1em 2em;
    background-color: #0b0a0a;
    border-radius: 8px;
    box-shadow: var(--brightwick-shadow);
    border: 1px solid var(--brightwick-red);
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

  .alt-contact:hover {
    box-shadow: var(--brightwick-shadow);
  }

  @media (max-width: 1000px) {
    .services-container {
      width: 90vw;
      flex-wrap: wrap;
    }

    .contact-container {
      display: flex;
      flex-wrap: wrap;
    }
  }
  
</style>
