<script lang="ts">
	import Nav from "$lib/Nav.svelte";
  import Footer from "$lib/Footer.svelte";
  import Background from "$lib/Background.svelte";
</script>

<div class="page-wrap">
  <Nav />
  <div class="content-wrap">
    <slot></slot>
    <Footer />
  </div>
  <Background />
</div>

<style>
</style>