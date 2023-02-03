<script>
  import { TwitterLogo, ClipboardText } from "phosphor-svelte";
  import Text from "./Text.svelte";
  import ToTop from "./ToTop.svelte";
</script>

<footer>
  <div class="left">
    <Text text={"m2 Ⓒ 2023"} />
    <Text text={"coded by trev"} />
    <div class="twitter-text">
      <TwitterLogo weight={"fill"} />
      <Text text={"view me on twitter"}/>
    </div>
    <div class="tos-text">
      <ClipboardText weight={"fill"}/>
      <Text text={"view TOS"} />
    </div>
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
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    opacity: 0.3
  }
  .right {
    display: flex;
    flex-direction: row;
  }
  .twitter-text {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 1rem;
  }
  .tos-text {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 1rem;
  }
</style>