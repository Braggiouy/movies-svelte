<script>
  import Movie from './Movie.svelte'
  let value = "";
  let totalMovies = []
  let loading = true
  const handleInput = (event) => {
    value = event.target.value;
  };

  $: if (value.length > 2) {
    loading = true
    async function fetchMovies() {
      // waits until the request completes...
      const response = await fetch(`http://www.omdbapi.com/?s=${value}&apikey=3b970e59`)
      const apiResponse = await response.json()
      totalMovies = apiResponse.Search || []
      loading = false
    }
    fetchMovies ()
  }
  
</script>

<main>
<input 
 placeholder="Search for a movie"
 value = {value} 
 on:input={handleInput} />

{#if loading}
<strong>Loading ...</strong>
{:else}
  {#each totalMovies as {Title, Poster, Year} , index}
    <Movie
    index = {index}
    title = {Title}
    poster = {Poster}
    year = {Year}/>
{:else}
<strong>We found no movies</strong>
{/each}
{/if}
  <!-- {  
  totalMovies.length > 0 ? `We found ${totalMovies.length} movies` : 'We found no movies'
      
  } -->

</main>