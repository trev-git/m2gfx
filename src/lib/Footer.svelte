<script>
  import { TwitterLogo, ClipboardText } from "phosphor-svelte";
  import Text from "./Text.svelte";
  import ToTop from "./ToTop.svelte";
</script>

<footer>
  <div class="left">
    <Text text={"m2 Ⓒ 2023"} />
    <Text text={"coded by trev"} href={"https://github.com/trev-git"}/>
    <Text text={"view me on twitter"} href={"https://twitter.com/mattsquare_"} icon={TwitterLogo}/>
    <Text text={"view TOS"} href={"tos"} icon={ClipboardText}/>
  </div>
  <div class="right">
    <ToTop />
  </div>
</footer>

<style>
  footer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 1rem 3rem;
    height: 64px;
    color: white;
  }
  .left {
    display: inline-flex;
    gap: 3rem;
  }
  .right {
    display: flex;
    flex-direction: row;
  }
</style>