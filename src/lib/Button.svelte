<script lang="ts">
  import { ShoppingCartSimple } from "phosphor-svelte"
	import CaretRight from "$lib/Icons/CaretRight.svelte";
  
  export let text: string = 'button text';
  export let style: '' | 'outlined' | 'secondary' = '';
  export let icon = ShoppingCartSimple;
  export let link: string = '/';

  const iconSize: string = '1.5rem';
</script>

<div class="button-container">
  <a class={'button ' + style} href={link}>
    <div class="button-icon-cluster">
      <svelte:component this={icon} color="currentColor" weight="fill" size={iconSize} />
      <CaretRight color="currentColor" size=".5rem" />
    </div>
    <p class="button-text">
      {text}
    </p>
  </a>
  <svg width="215" height="64" viewBox="0 0 215 64" fill="none" xmlns="http://www.w3.org/2000/svg">
    <rect x="2" y="2" width="211" height="60" rx="30" stroke="currentColor" stroke-width="4" stroke-linecap="round" stroke-dasharray="20 10"/>
  </svg>
</div>

<style>
  .button-container {
    position: relative;
  }

  .button-icon-cluster {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    column-gap: 0.5rem;
    row-gap: 0.5rem;
  }

  .button {
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
    padding-block: 0.75rem;
    padding-inline: 2rem;
    border-radius: 1000px;
    color: var(--secondary-two);
    background-color: var(--accent-two);
    box-shadow: 0 2px 130px 0 var(--accent-two-16);
    -webkit-transition: .2s ease;
    transition: .2s ease;
  }

  .button:hover {
    padding-inline: 3rem;
    box-shadow: 0 2px 130px 0 var(--accent-two-50);
  }
  
  svg {
    color: var(--accent-two);
    position: absolute;
    left: -.5rem;
    top: -.5rem;
    z-index: -5;
  }

  .button.outlined {
    background-color: transparent;
    color: var(--secondary);
    outline: 0.15rem solid var(--secondary);
    box-shadow: none;
  }

  .button.outlined + svg {
    display: none;
  }

  .button.outlined:hover {
    box-shadow: none;
  }

  .button.secondary {
    background-color: var(--secondary);
    box-shadow: 0 2px 130px 0 var(--secondary-16);
  }

  .button.secondary + svg {
    color: var(--secondary);
  }

  .button.secondary:hover {
    box-shadow: 0 2px 130px 0 var(--secondary-50);
  }
</style>