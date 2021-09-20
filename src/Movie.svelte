<script>
  export let title, poster, year;
</script>

<div class="movieBox">
  <div class="description">
    <p>
      {#if 2021 - year < 5}
        <i>🆕</i>
      {/if}
      {year} - {title}
    </p>
  </div>
  <img src={poster} alt={title} />
</div>

<style>
  .movieBox {
    display: inline-flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    border: 2px solid black;
    box-shadow: 1px -5px 12px 0px rgba(0, 0, 0, 0.4);
    -webkit-box-shadow: 1px -5px 12px 0px rgba(0, 0, 0, 0.4);
    -moz-box-shadow: 1px -5px 12px 0px rgba(0, 0, 0, 0.4);
    border-radius: 10px;
    width: 300px;
    margin: 1px;
    background-color: #81d2c7;
  }

  .description {
    margin: 10px;
    padding: 2px;
  }

  img {
    object-fit: cover;
  }
</style>
