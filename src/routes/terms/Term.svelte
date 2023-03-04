<script lang="ts">
  export let number: number;
  export let title: string;
  export let items: string[];
  export let paragraphDisplay: boolean = false;
</script>

<div class="terms">
  <div class="title">
    <h2 class="number bold-text">//{number}</h2>
    <h2 class="title bold-text">{title}</h2>
  </div>
  <div class="points">
    <ul>
      {#each items as item}
        <li class="normal-text">{item}</li>
      {/each}
    </ul>
  </div>
  {#if paragraphDisplay}
    <p class="bold-text paragraph">
      By commissioning me, you agree that you have read and accepted all the terms described herein.
    </p>
  {/if}
</div>

<style>
  .title {
    display: inline-flex;
    gap: 1rem;
    align-items: center;
  }
  h2 {
    font-family: 'Poppins';
    font-weight: 900;
    font-size: 2rem;
  }
  .number {
    font-family: 'StretchProV2';
  }
  ul {
    padding-left: 1rem;
    margin: 0;
  }
  .points {
    margin-top: 1.5rem;
  }
  .paragraph {
    margin-top: 1.5rem;
  }
</style>