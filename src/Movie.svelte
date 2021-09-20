<script>
  export let title, poster, year;
</script>

<div class="movieBox">

  <p>
    {#if 2021 - year < 5}
    <i>🆕</i>
    {/if}
  {year} - {title}
  </p>
  <img src={poster} alt={title} />

</div>

<style>
.movieBox {
  display: inline-flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  border: 1px solid red;
  width: 300px;
  margin: 5px;
}


</style>
