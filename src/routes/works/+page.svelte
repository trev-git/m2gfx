<script>
	import Button from "$lib/Button.svelte";
	import Works from "$lib/Works.svelte";
	import { PaperPlaneTilt } from "phosphor-svelte";
</script>

<section class="one">
  <div class="text">
    <h1>Past projects</h1>
    <p>Here are some of my earlier works, to give you an idea of what I can offer you!</p>
  </div>
  <Button text={"place your order"} color={"#5ee2bb"} icon={PaperPlaneTilt} href={"order"}/>
</section>
<section class="two">
  <div class="year">
    <h2>2023</h2>
    <img src="caret-right-white.svg"/>
  </div>
  <Works />
</section>
<section class="three">
  <div class="year">
    <h2>2022</h2>
    <img src="caret-right-white.svg"/>
  </div>
  <Works />
</section>

<style>
  h1 {
    font-family: 'Stretch Pro V2';
    font-size: 2rem;
  }
  h2 {
    margin: 0;
  }
  p {
    font-family: 'Poppins';
    font-weight: 700;
    margin: 0;
  }
  .text {
    width: 60%;
    margin-block: 4rem;
  }
  .year {
    display: inline-flex;
    font-family: 'Poppins';
    gap: 1rem;
  }
  .one {
    margin-top: 6rem;
  }
  .two {
    margin-top: 4rem;
  }
</style>