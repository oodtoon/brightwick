<script lang="ts">
  import backgroundImg from "$lib/images/podcastStill_1.1.1.png";

</script>

<div class="landing-img-container">
  <div class="list">
    <div class="recording-container">Rec
      <div class="recording-circle"></div>
    </div>
    <ul>
      <li>Podcasts</li>
      <li>Live Meetings</li>
      <li>Internal Training Videos</li>
    </ul>
    <div>Professional recording, streaming, and editing for you</div>
  </div>
  <div class="landing-img" style:background-image={`url(${backgroundImg})`}></div>
</div>

<style>
  .landing-img-container {
    position: relative;
    width: 100vw;
    height: 100vh;
  }

  .list {
    position: absolute;
    top: 30%;
    left: 50%;
    transform: translateX(-50%);
    z-index: 2;
    padding: 1em;
    background-color: rgba(0, 0, 0, 0.475);
    border-radius: 8px;
    border: 3px solid var(--brightwick-red);
  }

  li {
    font-size: 32px;
  }

  li::marker {
    color: var(--brightwick-red)
  }
  .landing-img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-size: cover;
    background-repeat: no-repeat;
    opacity: 0.5;
    z-index: 1;
  }

  .recording-container {
    position: absolute;
    left: 80%;
    display: flex;
    align-items: center;
    gap: .5em;
  }

  .recording-circle {
    content: "";
    background-color: red;
    height: 10px;
    width: 10px;
    border-radius: 50% 50%;
  }

  @media (max-width: 500px) {
    .list {
      top: 15%;
      width: 80vw;
    }
  }
</style>
