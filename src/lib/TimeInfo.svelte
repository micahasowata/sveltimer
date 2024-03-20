<script>
  import Footer from "./Footer.svelte";
  const timeInUTC = new Date().getTime().toLocaleString();
  let timeInfo = `It has been ${timeInUTC} milliseconds since January 1 1970`;

  const handleClick = () => {
    setInterval(() => {
      timeInfo = `Time is ${new Date().getUTCHours()}h : ${new Date().getUTCMinutes()}m : ${new Date().getUTCSeconds()}s`;
    }, 1000);
  };
</script>

<div class="flex-1">
  <div>
    <h2>
      {timeInfo}<sup>*</sup>
    </h2>
  </div>

  <button on:click={handleClick}>Clean it up</button>
</div>

<Footer />
