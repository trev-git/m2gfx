<script lang="ts">
  export let price: string;
  export let name: string;
  export let description: string;
  export let value: string = '';
</script>

<div class="price-listing">
  <p class="price">{price}</p>
  <div class="block-container">
    <div class="price-title">
      <h2>
        {name}
      </h2>
      <h2 class="value">{value}</h2>
    </div>
    <p class="description">
      {description}
    </p>
  </div>
</div>

<style>
  .price-listing {
    display: flex;
    align-items: center;
  }

  .price-title {
    display: flex;
    gap: 1rem;
  }

  p {
    font-family: Poppins, sans-serif;
  }

  p.price {
    display: flex;
    font-weight: 900;
    font-size: 2rem;
    min-width: 3.5em;
  }

  p.description {
    font-size: 1rem;
    font-weight: 700;
  }

  h2.value {
    color: var(--secondary-32)
  }
</style>
