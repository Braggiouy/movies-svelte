<script>
  export let title, poster, year;
</script>

<article>
  <img src={poster} alt={title} />
  <h3>{title}</h3>
  <span>{year}</span>
  {#if 2021 - year < 5}
    <i>🆕</i>
  {/if}
</article>

<style>
  article {
    display:flex;
    justify-content: center;
    align-items: center;
    border: 1px solid red;
    border-radius: 4px;
    margin-bottom: 8px;
    padding: 16px;
  }

  h3 {
    font-size: 24px;
    margin-bottom: 4px;
  }
</style>
