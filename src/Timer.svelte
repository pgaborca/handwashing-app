<script>
  import ProgressBar from "./ProgressBar.svelte";

  const totalseconds = 8;
  let secondsleft = totalseconds;
  let isRunning = false;
  let progress = 0;
  $: progress = ((totalseconds - secondsleft) / totalseconds) * 100;

  function startTimer() {
    isRunning = true;
    let timer = setInterval(() => {
      secondsleft -= 1;
      if (secondsleft == 0) {
        clearInterval(timer);
      }
    }, 1000);
  }
</script>

<style>
  h2 {
    margin: 0;
  }

  .start {
    width: 100%;
    background-color: brown;
    color: white;
    height: 3em;
    margin: 1em;
  }

  .start[disabled] {
    background-color: grey;
    cursor: not-allowed;
  }
</style>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds left: {secondsleft}</h2>
</div>

<ProgressBar {progress} />

<div bp="grid">
  <button disabled={isRunning} class="start" on:click={startTimer}>
    Start
  </button>
</div>
