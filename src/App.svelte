<script>
  import Counter from "./Counter.svelte";
  import Input from "./Input.svelte";

  const commonProps = { maxCounter: 5 };
</script>

<main>
	<h1>Search Movies 🍿</h1>
  <Input />
  <Counter count={4} />
  <Counter maxCounter={8} />
  <Counter maxCounter={6} />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	h1 {
		font-size: 32px;
	}
</style>
