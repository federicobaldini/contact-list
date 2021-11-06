<script>
	let name = 'Fede';
  let age = 24;

  /*
    whenever the name value change, this marker
    tells Svelte to follow the change and put into uppercaseName

    let uppercaseName; is not required!
  */
  $: uppercaseName = name.toUpperCase();

  const incrementAge = () => {
    age += 1;
  };

  const changeName = () => {
    name = 'Federico'
  };
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {uppercaseName}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<button on:click="{changeName}">Change Name</button>
