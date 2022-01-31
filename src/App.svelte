<script lang="ts">
import { prevent_default } from "svelte/internal";

	let names: string[] = ['Harvey', 'Bao', 'Michael'];
	let name: string;
	const handleOnSubsmit = () => {
		names = [...names, name];
	}
</script>

<main>
		<input bind:value={name}>
		<button on:click={handleOnSubsmit}>Submit</button>
	<ul>
		{#each names as name}
			<li>{name}</li>
		{/each}
	</ul>

</main>
<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>