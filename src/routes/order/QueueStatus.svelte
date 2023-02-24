<script lang="ts">
  export let style: 'open' | 'closed' | 'selective' = 'open';
</script>

<div class="queue-status {style}">
  <p class="normal-text">order status:</p>
  <p class="bold-text">{style}</p>
</div>

<style>
  .queue-status {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    border-radius: 200px;
    outline: solid 4px var(--accent-two);
    outline-offset: 4px;
    background-color: var(--accent-two);
    padding: 0.5rem 2rem;
    gap: 1rem;
  }
  p {
    color: var(--secondary-two)
  }
  .closed {
    background-color: var(--accent);
    outline: solid 4px var(--accent)
  }
  .selective {
    background-color: var(--secondary);
    outline: solid 4px var(--secondary);
  }
</style>