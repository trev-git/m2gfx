<script lang="ts">
  import { CaretRight, ShoppingCartSimple, PaperPlaneTilt, FilmStrip, ClipboardText } from "phosphor-svelte";
  export let text: string;
  export let color: string = "white";
  export let icon = ShoppingCartSimple;
  export let border: boolean = true;
  export let href: string;
</script>

{#if (border)}
<a {href} type="button" class="btn" style="--color: {color}; outline: 4px solid {color}">
  <div class="icons">
    <svelte:component this={icon} weight={"fill"} color={"black"} size={24}/>
    <img src="caret-right.svg" alt="caret"/>
  </div>
  <p>{text}</p>
</a>
{:else}
<a {href} type="button" class="btn" style="--color: {color};">
  <div class="icons">
    <svelte:component this={icon} weight={"fill"} color={"black"} size={24}/>
    <img src="caret-right.svg" alt="caret"/>
  </div>
  <p>{text}</p>
</a>
{/if}

<style>
  .btn {
    all: unset;
    display: inline-flex;
    align-items: center;
    color: black;
    background-color: var(--color);
    font-family: 'Poppins';
    font-size: 1rem;
    font-weight: 800;
    line-height: 1.5rem;
    padding-inline: 2rem;
    padding-block: 12px;
    border-radius: 10rem;
    outline-offset: 6px;
    gap: 1.5rem;
    cursor: pointer;
    transition: .2s;
  }
  .btn:hover {
    transition: .2s;
    padding-inline: 3rem;
    box-shadow: 0 2px 130px 0 rgba(94, 226, 187, 0.5);
  }
  p {
    margin: 0;
  }
  .icons {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }
</style>