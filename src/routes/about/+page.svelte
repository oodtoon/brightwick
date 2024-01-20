<script lang="ts">
  import Container from "$lib/components/Container.svelte";
  import Title from "$lib/components/Title.svelte";
  import Partner from "$lib/components/Partner.svelte";

  let kevinBioParagraphs=["Kevin has been producing video marketing material for companies for the past 4 years. He is extremely experienced with video production and audio capture.", "Aside from producing, Kevin also helps you get set up with the correct video package you need."]
  let brodyBioParagraphs=["Brody is an experienced video editor that has also produced videos and podcasts himself. He prides himself on making sure that every customer is excited of the final product.", "Brody also works as a Project Manager for the process. When you receive services and need changes to your edit, Brody will be able to help you out."]
</script>

<Container>
  <Title title="About" />
  <div class="about">
    <span class="company-name">Bright Wick Productions</span> is a video productions company local to
    Chicago. We film podcasts, internal training videos, and internal news letters.
    We also stream live meetings in case you in an extra something special on your
    next company meeting or sales call with a big client.
  </div>
  <Partner name="Kevin" paragraphs={kevinBioParagraphs}/>
  <Partner name="Brody" paragraphs={brodyBioParagraphs} />
</Container>

<style>
  .about {
    max-width: 800px;
    margin: auto;
    font-size: 20px;
  }

  .company-name {
    text-decoration: underline solid var(--brightwick-red);
  }
</style>
