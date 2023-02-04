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
      <p>I'm a graphics artist from Romania, helping both Creators and Streamers improve their viewers' experience through all things design!</p>
    </div>
    <img src="Gaming_Overlay_Preview.png" alt="img" />
  </div>
  <div class="btn">
    <Button text={"view my services"} href={"order"}/>
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
  <div class="header">
    <p class="view-some">Are you interested in getting something for yourself?</p>
  </div>
  <Button text={"commission from me"} href={"order"}/>
</section>

<style>
  .textimg {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  .text {
    color: white;
    width: 60%;
  }
  img {
    width: 40%;
    height: auto;
    object-fit: contain;
    border-radius: 2rem;
    transform: perspective(1000px) rotateX(5deg) rotateY(-10deg);
  }
  h1 {
    font-family: 'Stretch Pro V2';
    font-size: 4rem;
    margin: 0;
  }
  p {
    font-family: 'Poppins';
    font-weight: 700;
    margin: 0;
  }
  .btn {
    margin-block: 4rem;
  }
  .header {
    display: flex;
    margin-block: 2rem;
    flex-direction: row;
    justify-content: space-between;
  }
  .view-some {
    color: white;
  }
  .view-more {
    all: unset;
    font-family: 'Poppins';
    font-weight: 500;
    padding: 0.25rem 1rem;
    background-color: white;
    color: black;
    cursor: pointer;
    border-radius: 100rem;
  }
  .top {
    margin-block: 6rem;
  }
</style>