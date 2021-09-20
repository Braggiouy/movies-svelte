<!-- Javascript -->
<script>
  import Counter from "./Counter.svelte";
  import Input from "./Input.svelte";

  const commonProps = { maxCounter: 5 };
</script>

<!-- HTML -->
<h1>Search Movies 🍿</h1>
<Input />

<div>
  <Counter count={4} />
  <Counter maxCounter={8} />
  <Counter maxCounter={6} />
</div>

<!-- CSS -->
<style>
	div {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	/* section {
		display: flex;
		align-items: center;
		flex-direction: row;
	} */
	
	h1 {
		font-size: 32px;
	}


</style>
