<script>
	import Nav from "$lib/Nav.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<div id="content">
  <Nav />
  <slot></slot>
  <Footer />
</div>

<style>
  #content {
    max-width: 1920px;
    margin: auto;
    background-color: black;
    background-image: url(gradient.svg);
    background-position: 50% 100%;
    background-repeat: no-repeat;
    background-size: 100%, 10%;
  }
</style>