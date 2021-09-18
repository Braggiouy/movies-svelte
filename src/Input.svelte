<script>
  let value = "";
  let totalMovies = []
  const handleInput = (event) => {
    value = event.target.value;
  };

  $: if (value.length > 2) {
    async function fetchMovies() {
      // waits until the request completes...
      const response = await fetch(`http://www.omdbapi.com/?s=${value}&apikey=3b970e59`)
      const apiResponse = await response.json()
      totalMovies = apiResponse.Search
    }
    fetchMovies ()
      }
    
</script>

<input {value} on:input={handleInput} />
