<script lang="ts">
	import { onMount } from "svelte";

  export let style: 'open' | 'closed' | 'selective' = 'open';

  let divWidth: number;
  let divHeight: number;

  $: borderWidth = divWidth + 12;
  $: borderHeight = divHeight + 12;

  $: spinSpeed = 0.5;
  $: spinOffset = 0;

  onMount(() => {
    let frame = requestAnimationFrame(loop);

    function loop() {
      frame = requestAnimationFrame(loop);

      spinOffset = spinOffset - spinSpeed;
    }

    return (()=> {
      cancelAnimationFrame(frame);
    })
  })
</script>

<div class="order-status-container">
  <div class={"order-status " + style} bind:clientWidth={divWidth} bind:clientHeight={divHeight}>
    <p class="normal-text">order status:</p>
    <p class="bold-text">{style}</p>
  </div>
  <svg width={borderWidth + 4} height={borderHeight + 4} viewBox="0 0 {borderWidth + 4} {borderHeight + 4}" fill="none" xmlns="http://www.w3.org/2000/svg">
    <rect x="2" y="2" width={borderWidth} height={borderHeight} rx="26" stroke="currentColor" stroke-width="4" stroke-linecap="round" stroke-dasharray="56 10 36 10 8 10 34 10" stroke-dashoffset={spinOffset}/>
  </svg>
</div>

<style>
  .order-status-container {
    position: relative;
  }

  .order-status {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    border-radius: 200px;
    color: var(--secondary-two);
    background-color: var(--accent-two);
    padding: 0.5rem 2rem;
    gap: 1rem;
    box-shadow: 0 2px 130px 0 var(--accent-two-16);
  }
  
  svg {
    color: var(--accent-two);
    position: absolute;
    left: -.5rem;
    top: -.5rem;
    z-index: -5;
  }

  .order-status.closed {
    background-color: var(--accent);
  }

  .order-status.closed + svg {
    color: var(-accent);
  }

  .order-status.selective {
    background-color: var(--secondary);
  }

  .order-status.selective + svg {
    color: var(--secondary);
  }
</style>