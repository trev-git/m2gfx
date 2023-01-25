<script>
  import { FilmStrip, PaperPlaneTilt } from "phosphor-svelte";
  import Button from "./Button.svelte";
  import ButtonTos from "./ButtonTOS.svelte";
  import Assets from "./order/Assets.svelte";
import Queue from "./order/Queue.svelte";
  import Services from "./order/Services.svelte";


</script>

<div class="content">
  <div class="queue">
    <h1 class="header">Order from me</h1>
    <Queue/>
  </div>
  <p class="text">
    Here are some estimates for my most popular services. If the status is <br/>
    OPEN, you can contact me and we'll start discussing the details of <br/>
    your project right away!
  </p>
  <div class="btns">
    <Button text="place your order" icon={PaperPlaneTilt} color={"#5ee2bb"}/>
    <Button text="view examples" icon={FilmStrip} border={false}/>
  </div>
  <Assets />
  <Services />
  <ButtonTos />
  <Button text={"place your order"} border={true} color={"#5ee2bb"}/>
</div>

<style>
  .content {
    padding: 0 100px;
    margin: 50px 0;
  }
  .header {
    font-family: "Stretch Pro V2";
    font-weight: 700;
  }
  .text {
    font-family: "Poppins";
    font-weight: 700;
    margin-bottom: 5rem;
  }
  .queue {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .btns {
    display: flex;
    width: 70%;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-bottom: 5rem;
  }
</style>