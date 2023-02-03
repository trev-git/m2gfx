<script lang="ts">
  import { CaretRight, ShoppingCartSimple, PaperPlaneTilt, FilmStrip, ClipboardText } from "phosphor-svelte";
  export let text: string;
  export let color: string = "white";
  export let icon = ShoppingCartSimple;
  export let border: boolean = true;
</script>

{#if (border)}
<div class="btn" style="background-color: {color}; --color: {color}">
  <!-- <ShoppingCartSimple color={"black"} weight={"fill"} size={"18"}/> -->
  <svelte:component this={icon} color={"black"} weight={"fill"} size={"18"}/>
  <img class="caret-right" src="caret-right.svg" alt="right caret"/>
  <a href="#">{text}</a>
</div>
{:else}
<div class="btn" style="background-color: {color}; --color: rgba(0,0,0,0)">
  <!-- <ShoppingCartSimple color={"black"} weight={"fill"} size={"18"}/> -->
  <svelte:component this={icon} color={"black"} weight={"fill"} size={"18"}/>
  <img class="caret-right" src="caret-right.svg" alt="right caret"/>
  <a href="#">{text}</a>
</div>
{/if}

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700;900&display=swap');
  .btn {
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 15rem;
    flex-grow: 1;
    padding: 0.5rem 1rem;
    border-radius: 200px;
    outline: solid 4px var(--color);
    outline-offset: 6px;
    margin-right: 2rem;
  }
  a {
    font-family: "Poppins";
    text-decoration: none;
    font-weight: 700;
    color: black;
    margin-left: 20px;
  }
  a:hover {
    color: black;
  }
  .caret-right {
    margin-left: 5px;
  }
</style>