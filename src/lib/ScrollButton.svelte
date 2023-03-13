<script lang="ts">
  import CaretRight from "$lib/Icons/CaretRight.svelte";

  function toTop() {
    window.scrollTo({ top: 0, behavior: "smooth"});
  }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="scroll-button" on:click={toTop}>
  <div class="circle">
    <div class="caretbox">
      <CaretRight size="0.75rem" />
    </div>
  </div>
  <p class="button-text ">
    back to the top
  </p>
</div>

<style>
  .scroll-button {
    pointer-events: all;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    row-gap: 1rem;
    column-gap: 1rem;
    cursor: pointer;
  }
  
  .scroll-button > p {
    opacity: 0;
  }

  .scroll-button:hover > .circle {
    transform: scale(1.2, 1.2);
  }

  .scroll-button:hover > p {
    opacity: 1;
  }

  .circle {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    padding: 1rem;
    border-radius: 50%;
    background-color: var(--secondary-16);
    transition: transform .2s ease;
  }

  p {
    transition: opacity .3s ease;
  }

  .caretbox {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    transform: rotate(-90deg);
  }
</style>