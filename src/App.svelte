<script lang="ts">
const webs : { [key : string] : string } = {
  Info: "/info.html"
};

function goto(path : string) {
  window.location.href = path;
}
</script>

<main>
  <span id="blackbox">
    <p>so.. this is my neocities.. i pretty much host websites here!</p>
  </span>

  <h1 class="title">THE SITES!</h1>

  <div id="websites_container">

    {#each Object.entries(webs) as [key, value]}
    <span class="container">
      <h2 class="container_text">{key}</h2>
      <br>
      <button onclick={() => goto(value)}>Redirect me to that page!</button>
    </span>
    {/each}
  </div>

  <div class="bottom_a_hrefs">
    <a href="https://noobogonis.neocities.org">
      <img src="https://noobogonis.neocities.org/8831.png" alt="noobogonis's website">
    </a>
    <a href="https://caterzzz.neocities.org">
      <img src="https://caterzzz.neocities.org/assets/8831.png" alt="caterzzz's website">
    </a>
  </div>
</main>
