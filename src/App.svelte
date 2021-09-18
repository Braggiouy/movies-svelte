<script>
	export let count;
	function increase () {
		if(count < 10){
			count ++
		}
	}
	function decrease () {
		if(count > 0 ){
			count --
		}
	}
</script>

<main>
	<h1>Amount {count}</h1>
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