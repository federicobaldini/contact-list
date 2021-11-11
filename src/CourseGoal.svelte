<script>
  export let courseGoal;
</script>

<style>
  .error {
    color: red;
  }
</style>

<div>
  <h1 class:error="{courseGoal.includes('!')}">{courseGoal}</h1>
</div>