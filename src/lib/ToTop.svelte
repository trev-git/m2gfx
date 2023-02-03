<script>
  import CaretUp from "phosphor-svelte/lib/CaretUp";
  function toTop() {
    window.scrollTo({ top: 0, behavior: "smooth"});
  }
</script>

<div class="to-top">
  <a class="to-top" on:click={toTop}>
    <p>back to the top</p>
    <div class="circle">
      <CaretUp color={"white"} size={"10"} weight={"bold"}/>
    </div>
  </a>
</div>

<style>
  .to-top {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin: 0 1rem;
  }
  p {
    font-family: "Poppins";
    font-weight: 900;
    margin: 0 20px;
  }
  .circle {
    position: relative;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .circle::before {
    position: absolute;
    content: "";
    width: 20px;
    height: 20px;
    border-radius: 50%;
    opacity: 0.2;
    background-color: white;
  }
  a {
    all: unset;
    cursor: pointer;
  }
  a > p {
    opacity: 0;
    transition: opacity 1s;
  }
  a:hover > p {
    opacity: 1;
    transition: opacity 1s;
  }
</style>
