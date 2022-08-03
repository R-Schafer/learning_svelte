<script>
import { each } from "svelte/internal";


	let users = [
		{
			id: '1',
			name: 'John'
		},
		{
			id: '2',
			name: 'Sara'
		},
		{
			id: '3',
			name: 'Charlie'
		}
	]

	function addUser(){
		users = [...users, {id: '4', name: 'Rainey'}]
	}
</script>

<main>
	{#each users as user (user.id)}
		<h3>{user.id}. {user.name}</h3>
	{/each}

	<button on:click={addUser}>Add new User</button>
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
		font-size: 4em;
		font-weight: 100;
	}
</style>