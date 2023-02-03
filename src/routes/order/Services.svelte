<script>
  import { PenNib, PlusCircle } from "phosphor-svelte";
  import Header from "./Header.svelte";
  import PriceListing from "./PriceListing.svelte";
</script>

<div class="content">
  <Header icon={PlusCircle} text={"Extra Services"}/>
  <div class="prices">
    <PriceListing price={"+100%"} name={"Rush Order"} description={"You can skip the queue and get your project done first. Only for a few clients at a time"}/>
    <PriceListing price={"$80"} name={"Social Media Graphic"} description={"Get event graphics done for your growth on social media"}/>
    <PriceListing price={"$200"} name={"Logo"} description={"Get a themed logo fitted around your style "}/>
    <PriceListing price={"$300"} name={"Animated Logo"} description={"Get an animated logo fitted around your style"}/>
  </div>
</div>

<style>
  .content {
    margin-bottom: 5rem;
  }
  .prices {
    display: grid;
    grid-template-columns: 0.5fr;
    gap: 1rem;
  }
</style>