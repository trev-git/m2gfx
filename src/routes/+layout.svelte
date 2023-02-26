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
  <ScrollButton />
  <Background />
</div>

<style>
</style>