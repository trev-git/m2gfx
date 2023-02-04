<script lang="ts">
  export let price: string;
  export let name: string;
  export let description: string;
</script>

<div class="content">
  <div class="div-price">
    <p class="price">{price}</p>
  </div>
  <div class="name-desc">
    <p class="name">{name}</p>
    <p class="description">{description}</p>
  </div>
</div>

<style>
  .content {
    display: inline-flex;
    font-family: "Poppins";
    justify-content: center;
    align-items: center;
  }
  .div-price {
    width: 20%;
  }
  p {
    margin: 0;
  }
  .price {
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 900;
    float: left;
    font-size: 1.5rem;
    margin-right: auto;
  }
  .name-desc {
    width: 80%;
    margin-left: 1rem;
  }
  .name {
    font-weight: 900;
    font-size: 1.25rem;
  }
  .description {
    font-weight: 700;
    font-size: 1rem;
  }
</style>
