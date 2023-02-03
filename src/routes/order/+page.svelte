<script>
  import { FilmStrip, PaperPlaneTilt } from "phosphor-svelte";
  import Button from "$lib/Button.svelte";
  import ButtonTos from "$lib/ButtonTOS.svelte";
  import Assets from "./Assets.svelte";
  import Queue from "./Queue.svelte";
  import Services from "./Services.svelte";
</script>

<section class="one">
  <div class="header">
    <h1>Order from me</h1>
    <Queue />
  </div>
  <p class="text">Here are some estimates for my most popular services. If the status is OPEN, you  can contact me and we'll start discussing the details of your project right away!</p>
  <div class="btns">
    <Button icon={PaperPlaneTilt} text={"place your order"} color={"#5EE2BB"}/>
    <Button border={false} text={"view examples"} icon={FilmStrip}/>
  </div>
</section>

<section class="two">  
  <Assets />
</section>

<section class="three">
  <Services />
</section>

<section class="four">
  <ButtonTos />
  <Button text={"place your order"} border={true} color={"#5ee2bb"}/>
</section>

<style>
  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 6rem;
  }
  h1 {
    font-family: 'Stretch Pro V2';
    font-size: 2rem;
    margin: 0;
  }
  .text {
    font-weight: 700;
    font-family: 'Poppins';
    width: 60%;
  }
  .btns {
    display: inline-flex;
    margin-block: 4rem;
  }
  .two {
    margin-bottom: 6rem;
  }
</style>