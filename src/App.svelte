<script>
  import time from "./assets/time.svg";
  import TimeInfo from "./lib/TimeInfo.svelte";
</script>

<main class="flex flex-col">
  <div>
    <img src={time} alt="app logo" />
  </div>

  <TimeInfo />
</main>
