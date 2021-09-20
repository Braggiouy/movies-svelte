<!-- Javascript -->
<script>
  import Counter from "./Counter.svelte";
  import Input from "./Input.svelte";

  const commonProps = { maxCounter: 5 };
</script>

<!-- HTML -->

<nav class="navbar">
<h1>Search Movies 🍿</h1>
</nav>
<Input />
<div class="counter">
  <Counter count={4} />
  <Counter maxCounter={8} />
  <Counter maxCounter={6} />
</div>


<!-- CSS -->
<style>


	.navbar {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}

	.counter {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		border: 2px solid #7389ae;
		border-radius: 10px;
		background-color: #B5BAD0;
	}

	h1 {
		font-size: 24px;
	}


</style>
