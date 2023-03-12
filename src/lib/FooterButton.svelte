<script lang="ts">
  import { TwitterLogo } from 'phosphor-svelte';

  export let text: string = '';
  export let icon = TwitterLogo;
  export let link: string = '/';
  export let newTab: boolean = false;

  const iconSize: string = '2rem';

  function openNewTab () {
    if (newTab) {
      return '_blank';
    }
    
    else {
      return '';
    }
  }
</script>

<a class="footer-button" href={link} target={openNewTab()}>
  <svelte:component this={icon} color="currentColor" weight="fill" size={iconSize} />
  {#if text !== ''}
    <p class="button-text">
      {text}
    </p>
  {/if}
</a>

<style>
  .footer-button {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    column-gap: 1.5rem;
    row-gap: 1.5rem;
    padding: 1.5rem;
    opacity: 0.3;
    -webkit-transition: opacity .2s ease;
    transition: opacity .2s ease;
    z-index: 1000;
  }

  .footer-button:hover {
    opacity: 1;
  }
</style>