<script>
  import CaretUp from "phosphor-svelte/lib/CaretUp";

  function toTop() {
    window.scrollTo({ top: 0, behavior: "smooth"});
  }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div on:click={toTop} class="to-top">
  <p>back to the top</p>
  <div class="circle">
    <CaretUp color={"white"} size={"32"} weight={"bold"}/>
  </div>
</div>

<style>
  .to-top {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 2rem;
  }
  .to-top > p {
    font-family: "Poppins";
    font-weight: 700;
    font-size: 1.5rem;
    padding-block: 14px;
    margin: 0;
    transition: 500ms;
    opacity: 0;
  }
  .to-top:hover > p {
    transition: 300ms;
    opacity: 1;
  }
  .circle {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    width: 4rem;
    height: 4rem;
  }
  /* .circle::before {
    position: absolute;
    content: '';
    width: 64px;
    height: 64px;
    background-color: white;
    opacity: 0.1;
    border-radius: 50%;
  } */
</style>
