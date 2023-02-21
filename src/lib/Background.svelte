<script lang="ts">

</script>

<div class="background-noise"></div>
<img
  src="/Background Gradient 1.png"
  alt="Background"
  class="background-gradient gradient-1"
>
<img
  src="/Background Gradient 2.png"
  alt="Background"
  class="background-gradient gradient-2"
>
<img
  src="/Background Gradient 3.png"
  alt="Background"
  class="background-gradient gradient-3"
>

<style>
  .background-noise {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: -10;
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    max-width: 100%;
    max-height: 100%;
    background-image: url("/Noise.png");
    background-size: auto;
    opacity: 0.06;
  }

  .background-gradient {
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: -10;
    width: 100%;
    height: 62.5rem;
  }
  
  .background-gradient.gradient-1 {
    left: auto;
  }

  .background-gradient.gradient-3 {
    right: auto;
  }
</style>