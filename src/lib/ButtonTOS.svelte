<script lang="ts">
  import { ClipboardText } from "phosphor-svelte";
  export let href = "tos";
  export let text = "view the terms that apply";
  export let icon = ClipboardText;
</script>

<a class="btn" {href}>
  <div class="icons">
    <svelte:component this={icon} color={"white"} weight={"fill"} size={"24"}/>
    <img class="caret-right" src="caret-right-white.svg" alt="right caret"/>
  </div>
  <p class="text">{text}</p>
</a>

<style>
  .btn {
    all: unset;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    border: 2px solid var(--secondary);
    padding-inline: 2rem;
    padding-block: 12px;
    border-radius: 1000px;
    cursor: pointer;
    gap: 1.5rem;
    transition: .2s;
  }
  .btn:hover {
    transition: .2s;
    padding-inline: 3rem;
  }
  .text {
    all: unset;
    font-family: "Poppins";
    font-weight: 700;
  }
  .caret-right {
    margin-left: 0.5rem;
  }
  .icons {
    display: inline-flex;
    align-items: center;
  }
</style>