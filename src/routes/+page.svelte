<script>
  import Button from "$lib/Button.svelte";
  import Works from "$lib/Works.svelte";
  import ButtonTos from "$lib/ButtonTOS.svelte";
	import KofiLogo from "$lib/KofiLogo.svelte";
	import { ShoppingCartSimple } from "phosphor-svelte";
</script>


<section class="intro">
  <div class="intro-layout">
    <div class="title-layout">
      <div class="text-layout">
        <h1 class="heading">Hi, <br /> I'm Matt</h1>
        <p class="desc">I’m a graphics artist from Romania, helping both Creators and Streamers improve their viewers’ experience through all things design!</p>
      </div>
      <div class="btns">
        <Button text={"services"} icon={ShoppingCartSimple} border={false} color={"#5ee2bb"} href={"order"}/>
        <ButtonTos href={"#"} icon={KofiLogo} text={"premade shop"}/>
      </div>
    </div>
    <div class="img-layout">
      <img src="Gaming_Overlay_Preview.png" alt="img" />
    </div>
  </div>
</section>

<section class="works">
  <div class="works-title">
    <p class="work">View some of my work</p>
    <a href="/works" class="view-more">view more</a>
  </div>
  <Works />
</section>

<section class="order">
  <p class="interested">Are you interested in getting something for yourself?</p>
  <div class="btn">
    <Button href={"/order"} icon={ShoppingCartSimple} border={false} text={"order from me"} color={"#5ee2bb"}/>
  </div>
</section>

<style>
  .intro {
    display: flex;
  }
  
  .intro-layout {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }

  .title-layout {
    display: flex;
    flex-direction: column;
    grid-column: 1 / 2;
    gap: 4rem;
  }

  .img-layout {
    grid-column: 2 / 3;
  }

  .text-layout {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  img {
    width: 100%;
    height: 100%;
    border-radius: 2rem;
    transform: perspective(5000px) rotateX(-15deg) rotateY(-5deg);
  }

  .heading {
    font-family: 'StretchProV2';
    font-size: 6rem;
    font-weight: 400;
    line-height: 6rem;
    margin: 0;
    margin-bottom: 2rem;
  }

  .desc {
    font-family: 'Poppins';
    font-weight: 500;
    font-size: 1rem;
    line-height: 1.5rem;
    margin: 0;
  }

  .btns {
    display: flex;
    gap: 2rem;
    max-width: 100%;
  }

  .works-title {
    display: flex;
    justify-content: space-between;
  }

  .work {
    font-family: 'Poppins';
    font-weight: 800;
    line-height: 1.5rem;
    margin: 0;
  }

  .view-more {
    all: unset;
    color: var(--secondary-two);
    background-color: var(--secondary);
    font-family: 'Poppins';
    font-weight: 800;
    line-height: 1.5rem;
    padding: 0.5rem 2rem;
    border-radius: 50rem;
    cursor: pointer;
    transition: .2s;
  }

  .view-more:hover {
    transition: .2s;
    padding-inline: 3rem;
    background-color: var(--accent-two);
    box-shadow: 0 1px 130px 0 rgba(94, 226, 187, 0.5);
  }

  .works {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .order {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .interested {
    font-family: 'Poppins';
    font-size: 1rem;
    font-weight: 800;
    margin: 0;
  }
</style>