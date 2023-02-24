<script lang="ts">
  export let style: 'open' | 'closed' | 'selective' = 'open';
</script>

<div class={"order-status " + style}>
  <p class="normal-text">order status:</p>
  <p class="bold-text">{style}</p>
</div>

<style>
  .order-status {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    border-radius: 200px;
    color: var(--secondary-two);
    outline: solid 4px var(--accent-two);
    outline-offset: 4px;
    background-color: var(--accent-two);
    padding: 0.5rem 2rem;
    gap: 1rem;
    box-shadow: 0 2px 130px 0 var(--accent-two-16);
  }
  
  .order-status.closed {
    background-color: var(--accent);
    outline: solid 4px var(--accent);
  }

  .order-status.selective {
    background-color: var(--secondary);
    outline: solid 4px var(--secondary);
  }
</style>