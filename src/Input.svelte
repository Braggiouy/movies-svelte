<!-- Javascript -->
<script>
  import Movie from "./Movie.svelte";
  let value = "";
  let response = [];

  const handleInput = (event) => {
    value = event.target.value;
  };

  $: if (value.length > 2) {
    response = fetch(`http://www.omdbapi.com/?s=${value}&apikey=3b970e59`)
    // .then((res) => !res.ok() && new Error("theref asfa fas hr hrt "))
      .then((res) => res.json())
      .then((apiResponse) => apiResponse.Search || []);
  }
</script>

<!-- HTML -->
<div class="inputBox">
<input placeholder="Search for a movie" value = {value} on:input={handleInput} />
</div>
{#await response}
  <strong>Loading ...</strong>
{:then movies}
  {#each movies as { Title, Poster, Year }, index}
    <Movie 
    index={index} 
    title={Title} 
    poster={Poster} 
    year={Year} 
    />
  {:else}
    <strong>We found no movies</strong>
  {/each}
{:catch error}
  <p>❌ There has been an {error}</p>
{/await}

<!-- CSS -->
<style>
.inputBox {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>