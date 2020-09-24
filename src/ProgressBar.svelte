<script>
  export let progress = 30;
</script>

<style>
  .progress-container {
    margin: 10px 0;
    border: solid #a09e9e 1px;
  }
  .progress-bar {
    height: 30px;
    background-color: greenyellow;
  }
</style>

<div bp="grid">
  <div bp="offset-5@md 4@md 12@sm" class="progress-container">
    <div class="progress-bar" style="width: {progress}%">
      <span class="st-only">{progress}%</span>
    </div>
  </div>
</div>
