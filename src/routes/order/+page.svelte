<script lang="ts">
  import { PaperPlaneTilt, FilmStrip, PlusCircle, Package, ClipboardText } from "phosphor-svelte";
  import Button from "$lib/Button.svelte";
	import Header from "./Header.svelte";
	import PriceListing from "./PriceListing.svelte";
	import QueueStatus from "./QueueStatus.svelte";

  type priceEntryList = { price: string, title: string, value?: string, desc: string }[];

  const pricesVtubers: priceEntryList = [
    {
      price: '$100',
      title: 'Stream Overlay',
      desc:  'For any kind of overlay, chatting or game overlays.'
    },
    {
      price: '$100',
      title: 'Starting / Ending Scenes',
      desc:  'Get graphics for the start, end and break scenes.'
    },
    {
      price: '$40',
      title: 'Minimal Overlay',
      desc:  'Get a minimal webcam border.'
    },
    {
      price: '+$40',
      title: 'Animations',
      desc:  'Get animations for each overlay or scene you\'ve ordered.'
    },
    {
      price: '+$10',
      title: 'Twitch Panels',
      desc:  'Get panels for your description on Twitch.'
    },
    {
      price: '$40',
      title: 'Banner',
      desc:  'Get a banner for your Twitter page, or YouTube channel.'
    },
    {
      price: '$110',
      title: 'Stream Schedule',
      desc:  'Get a customizable, editable stream schedule.'
    },
    {
      price: '$180',
      title: 'Chat Widget',
      desc:  'Get a custom-fitted, animated chat widget.'
    }
  ]

  const pricesPerks: priceEntryList = [
    {
      price: '+100%',
      title: 'Rush Order',
      desc:  'You can skip the queue and get your project done first. Limited availability.'
    },
    {
      price: '$60',
      title: 'Social Media Graphic',
      desc:  'Get event graphics done for your growth on social media.'
    },
    {
      price: '$200',
      title: 'Logo',
      desc:  'Get a themed logo fitted around your style.'
    },
    {
      price: '$300',
      title: 'Animated Logo',
      desc:  'Get an animated logo fitted around your style.'
    }
  ]

  const pricesPackages: priceEntryList = [
    {
      price: '$200',
      title: 'Basic',
      value: '-$60 Value',
      desc:  '1 + 1 Overlay / Scene, Set of 6 Twitch Panels'
    },
    {
      price: '$380',
      title: 'Animated',
      value: '-$100 Value',
      desc:  '1 + 1 + 1 Overlay / Scene, Animated, Set of 6 Twitch Panels'
    },
    {
      price: '$590',
      title: 'Complete',
      value: '-$140 Value',
      desc:  '2 + 2 Overlay / Scene, Animations, Set of 6 Twitch Panels, Stream Schedule'
    }
  ]
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
    {#each pricesVtubers as entry}
      <PriceListing price={entry.price} name={entry.title} description={entry.desc} />
    {/each}
  </div>
</div>

<div class="content layouted">
  <div class="heading">
    <Header text={"Other Perks"} icon={PlusCircle}/>
  </div>
  <div class="price-grid">
    {#each pricesPerks as entry}
      <PriceListing price={entry.price} name={entry.title} description={entry.desc} />
    {/each}
  </div>
</div>

<div class="content layouted">
  <div class="heading">
    <Header text={"Package Deals"} icon={Package}/>
  </div>
  <div class="price-grid">
    {#each pricesPackages as entry}
      <PriceListing price={entry.price} name={entry.title} value={entry.value} description={entry.desc} />
    {/each}
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
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .price-grid {
    display: -ms-grid;
    display: grid;
    width: 100%;
    grid-auto-flow: column;
    grid-auto-columns: 1fr;
    -ms-grid-columns: 1fr;
    grid-template-columns: 1fr;
    -ms-grid-rows: repeat(4, 0.25fr);
    grid-template-rows: repeat(4, 0.25fr);
    column-gap: 2rem;
    row-gap: 2rem;
  }
</style>