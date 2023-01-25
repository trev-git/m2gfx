<script>
  import { ClipboardText } from "phosphor-svelte";
</script>

<div class="btn">
  <ClipboardText color={"white"} weight={"fill"} size={"18"}/>
  <img class="caret-right" src="caret-right-white.svg" alt="right caret"/>
  <a class="text" href="/tos">view the terms that apply</a>
</div>

<style>
  .btn {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    outline: solid 4px white;
    outline-offset: 4px;
    padding: 0.5rem 2.56rem;
    border-radius: 200px;
    margin-bottom: 3rem;
    cursor: pointer;
  }
  .text {
    all: unset;
    font-family: "Poppins";
    font-weight: 700;
    margin-left: 1rem;
  }
  .caret-right {
    margin-left: 0.5rem;
  }
</style>