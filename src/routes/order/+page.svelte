<script>
  import { PaperPlaneTilt, FilmStrip, PlusCircle, Package, ClipboardText } from "phosphor-svelte";
  import Button from "$lib/Button.svelte";
	import Header from "./Header.svelte";
	import PriceListing from "./PriceListing.svelte";
	import QueueStatus from "./QueueStatus.svelte";
</script>

<div class="content grid">
  <div class="title-layout">
    <div class="title-text-layout">
      <div class="order-status-layout">
        <h1>Order from me</h1>
      </div>
      <p class="normal-text">
        Here are some estimates for my most popular services. If the 
        status is OPEN, you  can contact me and we&#x27;ll start discussing the 
        details of your project right away!
      </p>
      <p class="normal-text">
        Orders can be paid for either 50% upfront, 50% after approval, OR 100% upfront.
      </p>
    </div>
    <div class="_2rem-layout">
      <Button text={"contact"} icon={PaperPlaneTilt} link={"/contact"}/>
      <Button text={"other works"} icon={FilmStrip} style={"outlined"} link={"/works"}/>
    </div>
  </div>
  <div class="queue-status">
    <QueueStatus />
  </div>
</div>

<div class="content layouted">
  <div class="heading">
    <Header text={"VTuber/Streamer Assets"}/>
  </div>
  <div class="price-grid">
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
  </div>
</div>

<div class="content layouted">
  <div class="heading">
    <Header text={"Other Perks"} icon={PlusCircle}/>
  </div>
  <div class="price">
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."}/>
  </div>
</div>

<div class="content layouted">
  <div class="heading">
    <Header text={"Package Deals"} icon={Package}/>
  </div>
  <div class="price">
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."} value={"-$20 Value"}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."} value={"-$100 Value"}/>
    <PriceListing price={"$120"} name={"Stream Overlay"} description={"For any kind of overlay, chatting or game overlays."} value={"-$140 Value"}/>
  </div>
</div>

<div class="content layouted">
  <h3>Have you decided?</h3>
  <div class="_2rem-layout">
    <Button text={"get in touch"} icon={PaperPlaneTilt} link={"/contact"}/>
    <Button text={"read the terms"} icon={ClipboardText} style={"outlined"} link={"/tos"} />
  </div>
</div>

<style>
  .order-status-layout {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .price-grid {
    display: grid;
    width: 100%;
    grid-template-columns: repeat(2, 1fr);
    row-gap: 2rem;
  }
  .price {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
</style>