<script>
  export let src = null;
  export let alt = null;
</script>

<div class="rectangle">
  <img class="rectangle" {src} {alt}/>
</div>

<style>
  .rectangle {
    background-color: white;
    aspect-ratio: 16 / 9;
    border-radius: 1rem;
    width: 100%;
    height: 100%;
  }
</style>
