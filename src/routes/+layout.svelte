<script lang="ts">
	import Nav from "$lib/Nav.svelte";
  import Footer from "$lib/Footer.svelte";
  import Background from "$lib/Background.svelte";
	import ScrollButton from "$lib/ScrollButton.svelte";
</script>

<div class="page-wrap">
  <Nav />
  <div class="content-wrap">
    <slot></slot>
    <Footer />
  </div>
  <div class="scroll-wrapper">
    <div class="wrapper-two">
      <ScrollButton />
    </div>
  </div>
  <Background />
</div>

<style>
  .scroll-wrapper {
    position: sticky;
    bottom: 3rem;
    padding-inline: 4rem;
    display: flex;
    justify-content: center;
  }
  .wrapper-two {
    max-width: 1920px;
    width: 100%;
    display: flex;
    justify-content: right;
  }
</style>