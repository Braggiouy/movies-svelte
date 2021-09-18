<script>
	export let count = 0;
	function increase () {
		if(count < 10){
			count ++
		}
	}
	function decrease () {
		if(count > 0 	){
			count --
		}
	}
</script>

<main>
	<p>Amount {count}</p>
	<button on:click={increase}>Increase</button> 
	<button on:click={decrease}>Decrease</button> 
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	p {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 1em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>