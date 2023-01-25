<script>
  import { CaretRight, ShoppingCart } from "phosphor-svelte";
  import style from "../app.css?inline"
  import Sex from "../assets/Sex.svelte";
  import Button from "./Button.svelte";
</script>

<div class="content">
  <div class="info">
    <div class="text">
      <h1 class="hi">Hi, <br/> I`m Matt</h1>
      <p class="bio">
        I'm a graphics artist from Romania, <br/>
        helping both Creators and Streamers improve <br/>
        their viewers' experience through all things design!
      </p>
    </div>
    <div class="image">
      <Sex />
    </div>
  </div>
</div>

<style>
  .content {
    padding: 0 100px;
    margin: 50px 0;
  }
  .hi {
    font-family: "Stretch Pro V2";
    font-size: 4rem;
    margin: 25px 0;
  }
  .info {
    margin: 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 0 25px 0;
  }
  .bio {
    font-family: "Poppins";
  }
  .btn-services{
    display: flex;
    justify-content: center;
    align-items: center;
    all: unset;
    border-radius: 50px;
    background-color: white;
  }
  a {
    text-decoration: none;
    font-family: "Poppins";
    color: black;
  }
  a:hover {
    color: black;
  }
</style>