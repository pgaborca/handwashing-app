<script>
  import ProgressBar from "./ProgressBar.svelte";
</script>

<style>
  h2 {
    margin: 0;
  }

  button {
    width: 100%;
    background-color: brown;
    color: white;
    height: 3em;
  }
</style>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds left: 12</h2>
</div>

<ProgressBar />

<button class="start">Start</button>
