<script>
	import Counter from './Counter.svelte'
	import Input from "./Input.svelte";

	const commonProps = {maxCounter : 5}
</script>

<main>
<Input/>
<Counter count = {4}></Counter>
<Counter maxCounter = {8}></Counter>	
<Counter maxCounter = {6}></Counter>
</main>