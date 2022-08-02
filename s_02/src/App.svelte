<script>
	let firstName = 'Jane'
	let lastName = 'Doe'
	let color = 'red'
	let showText = false

	$: name = firstName + ' ' + lastName

	function toggle() {
		color = color === 'red' ? 'green' : 'red'
		showText = !showText
	}

</script>

<main>
	<h1 style="color:{color}">Hello {name}!</h1>
	{#if showText}
		<p>I'm glad you are here</p>
	{/if}
	<button on:click={toggle}>Click Me</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
</style>