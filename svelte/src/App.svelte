<script>
	export let name;

	let rando
	$: result = Math.random
	function setRando(){
		rando = Math.random();
	}
</script>

<main>
	<h1>HOW ARE YA?! {name}!</h1>
	<p>{Math.round(rando) ? 'winner': "loser"}</p>
	<button on:click={setRando}>ROLL THE DICE</button>
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
		font-size: 10em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>