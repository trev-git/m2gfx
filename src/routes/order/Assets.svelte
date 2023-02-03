<script>
  import { PenNib } from "phosphor-svelte";
  import Header from "./Header.svelte";
  import PriceListing from "./PriceListing.svelte";
</script>

<div class="content">
  <Header icon={PenNib} text={"VTuber/Streamer Assets"}/>
  <div class="prices">
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlay"}/>
    <PriceListing price={"+$10"} name={"Twitch Panels"} description={"Get panels for your description on Twitch"}/>
    <PriceListing price={"$120"} name={"Starting/Ending Scenes"} description={"Get graphics for the start, end and break scenes"}/>
    <PriceListing price={"$50"} name={"Banner"} description={"Get a banner for your Twitter Page, or YouTube channel"}/>
    <PriceListing price={"$50"} name={"Minimal Overlay"} description={"Get a small webcam border"}/>
    <PriceListing price={"$120"} name={"Stinger Transition"} description={"Get animated transitions for scene swaps"}/>
    <PriceListing price={"$200"} name={"Animation Package"} description={"Get animations for all overlays you've ordered"}/>
    <PriceListing price={"$140"} name={"Schedule"} description={"Get a customizable, editable stream schedule"}/>
  </div>
</div>

<style>
  .content {
    margin-bottom: 2rem;
  }
  .prices {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }
</style>