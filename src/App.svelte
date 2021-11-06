<script>
	let name = 'Fede';
  let age = 24;

  /*
    whenever the name value change, this marker/label ('$:')
    tells Svelte to follow the change and put into uppercaseName

    let uppercaseName; is not required!
  */
  $: uppercaseName = name.toUpperCase();

  $: if (name === 'Federico') {
    age = 20;
  }

  const incrementAge = () => {
    age += 1;
  };

  const changeNameHandler = (event) => {
    const enteredName = event.target.value;
    name = enteredName;
  };
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {uppercaseName}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<!-- <input type="text" value="{name}" on:input="{changeNameHandler}"> -->
<!-- 
  do not abuse about this two-way data binding syntax
-->
<input type="text" bind:value="{name}">
