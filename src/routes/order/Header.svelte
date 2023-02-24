<script lang="ts">
	import { PenNib } from "phosphor-svelte";

  export let icon = PenNib;
  export let text: string;
</script>

<div class="header">
  <div class="icon">
    <svelte:component this={icon} weight={"fill"} color={"#5ee2bb"} size={32}/>
  </div>
  <h2>{text}</h2>
</div>

<style>
  .header {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    font-family: "Poppins";
    font-weight: 900;
    margin-bottom: 1rem;
    gap: 1rem;
  }
  h2 {
    color: var(--accent-two)
  }
</style>
