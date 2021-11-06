<script>
	export let name = 'Federico';
  export let age = 24;

  const incrementAge = () => {
    age += 1;
  }

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
