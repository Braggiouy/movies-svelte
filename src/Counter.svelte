<script>
  export let count = 0;
  export let maxCounter = 10;
  function increase() {
    count++;
  }
  function decrease() {
    count--;
  }

  $: isEvenOrOdd = count % 2 === 0 ? "Counter is even" : "Counter is Odd";
  // Manera de indicar que es una sentencia reactiva, que tiene que variar en cuanto uno de sus valores cambie.

  $: {
    if (count === maxCounter) {
      setTimeout(() => {
        count = 0;
      }, 500);
    }
  }
</script>

<main>
  <p>Amount {count}</p>
  <p>{isEvenOrOdd}</p>
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
