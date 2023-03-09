<script lang="ts">
  import Button from "$lib/Button.svelte";
  import NavButton from "$lib/NavButton.svelte";
  import KofiLogo from "$lib/Icons/KofiLogo.svelte";
  import ShowcaseContainer from "$lib/ShowcaseContainer.svelte";
</script>

<div class="content grid">
  <div class="title-layout">
    <div class=title-text-layout>
      <h1 class="title">
        Hi, <br> I&#x27;m Matt
      </h1>
      <p class="normal-text">
        I&#x27;m a graphics artist from Romania,
        helping both Creators and Streamers improve
        their viewers&#x27; experience through all things design!
      </p>
    </div>
    <div class="_2rem-layout vertical">
      <Button text="services" link="/order" />
      <Button text="premade shop" icon={KofiLogo} style="outlined"  link="https://ko-fi.com/mattsquare" newTab={true} />
    </div>
  </div>
</div>
<div class="content layouted">
  <div class="landing-works-link">
    <h3>
      View some of my work
    </h3>
    <NavButton text="view portfolio" style="active" link="/works" />
  </div>
  <ShowcaseContainer />
</div>
<div class="content layouted">
  <p class="bold-text">Are you interested in getting something for yourself?</p>
  <Button text={"commission from me"} link={"/order"} type={"button"} />
</div>
<style>
.landing-works-link {
  width: 100%;
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  -webkit-box-pack: space-between;
  -webkit-justify-content: space-between;
  -ms-flex-pack: space-between;
  justify-content: space-between;
}
</style>