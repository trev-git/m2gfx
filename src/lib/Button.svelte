<script lang="ts">
  import { ShoppingCartSimple } from "phosphor-svelte"
	import CaretRight from "$lib/Icons/CaretRight.svelte";
  
  export let text: string = 'button text';
  export let style: '' | 'outlined' | 'secondary' = '';
  export let icon = ShoppingCartSimple;
  export let link: string = '/';

  const iconSize: string = '1.5rem';
</script>

<a class={'button ' + style} href={link}>
  <div class="button-icon-cluster">
    <svelte:component this={icon} color="currentColor" weight="fill" size={iconSize} />
    <CaretRight color="currentColor" size=".5rem" />
  </div>
  <p class="button-text">
    {text}
  </p>
</a>

<style>
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

  .button.outlined {
    background-color: transparent;
    color: var(--secondary);
    outline: 0.15rem solid var(--secondary);
    box-shadow: none;
  }

  .button.outlined:hover {
    box-shadow: none;
  }

  .button.secondary {
    background-color: var(--secondary);
    box-shadow: 0 2px 130px 0 var(--secondary-16);
  }

  .button.secondary:hover {
    box-shadow: 0 2px 130px 0 var(--secondary-50);
  }
</style>