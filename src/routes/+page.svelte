<script>
  import Button from "$lib/Button.svelte";
  import Works from "$lib/Works.svelte";
</script>

<section class="top">
  <div class="textimg">
    <div class="text">
      <h1>
        Hi, <br/> I'm Matt
      </h1>
        <p class="desc">I'm a graphics artist from Romania,
          helping both Creators and Streamers improve
          their viewers' experience through all things design!</p>
    </div>
    <div class="img">
      <img src="Gaming_Overlay_Preview.png" alt="img" />
    </div>
  </div>
  <div class="btn">
    <Button text={"view my services"} href={"order"} color={"#5ee2bb"}/>
  </div>
</section>

<section class="middle">
  <div class="header">
    <p class="view-some">View some of my work:</p>
    <a class="view-more" href="#">View more</a>
  </div>
  <Works />
</section>

<section class="bottom">
  <div class="header2">
    <p class="view-some">Are you interested in getting something for yourself?</p>
  </div>
  <Button text={"commission from me"} href={"order"} color={"#5ee2bb"}/>
</section>

<style>
  .textimg {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .text {
    width: 50%;
    color: white;
  }
  .img {
    width: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  img {
    max-width: 100%;
    max-height: 100%;
    transform: perspective(1000px) rotateX(5deg) rotateY(-10deg);
  }
  h1 {
    font-family: 'Stretch Pro V2';
    font-size: 110px;
    margin-block: 2rem;
  }
  p {
    font-family: 'Poppins';
    font-size: 1.5rem;
    font-weight: 700;
    margin-block: 2rem;
  }
  .btn {
    margin-block: 4rem;
  }
  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

  }
  .view-some {
    margin: 0;
    padding-block: 0.5rem;
    font-size: 1.5rem;
    color: white;
  }
  .view-more {
    all: unset;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins';
    font-weight: 500;
    font-size: 1.5rem;
    padding: 0.5rem 2rem;
    background-color: white;
    color: black;
    cursor: pointer;
    border-radius: 100rem;
  }
  .top {
    margin-bottom: 16rem;
  }
  .middle {
    margin-bottom: 6rem;
  }
  .header2 {
    margin-bottom: 3rem;
  }
</style>