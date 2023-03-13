<script lang="ts">
  import MetaTitle from "$lib/MetaTitle.svelte";
  import Button from "$lib/Button.svelte";
  import NavButton from "$lib/NavButton.svelte";
  import KofiLogo from "$lib/Icons/KofiLogo.svelte";
  import ShowcaseContainer from "$lib/ShowcaseContainer.svelte";
</script>

<MetaTitle title="Home" />
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
  <div class="works-link">
    <h3>
      View some of my work
    </h3>
    <NavButton text="view portfolio" style="active" link="/works" />
  </div>
  <div class="works-grid">
    <div class="works-grid-column">
      <ShowcaseContainer />
      <div class="works-grid-row">
        <ShowcaseContainer />
        <ShowcaseContainer />
      </div>
    </div>
    <div class="works-grid-column">
      <ShowcaseContainer />
      <div class="works-grid-row">
        <ShowcaseContainer />
        <ShowcaseContainer />
      </div>
    </div>
  </div>
</div>
<div class="content layouted">
  <p class="bold-text">Are you interested in getting something for yourself?</p>
  <Button text={"commission from me"} link={"/order"} type={"button"} />
</div>
<style>
.works-link {
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

.works-grid {
  display: grid;
  justify-items: stretch;
  align-items: start;
  grid-auto-columns: 1fr;
  grid-template-columns: 1.25fr 1fr;
  grid-template-rows: auto;
  column-gap: 2rem;
  row-gap: 2rem;
}

.works-grid-column {
  display: grid;
  justify-items: stretch;
  align-items: start;
  grid-auto-columns: 1fr;
  grid-template-columns: 1fr;
  grid-template-rows: auto;
  column-gap: 2rem;
  row-gap: 2rem;
}

.works-grid-row {
  display: grid;
  justify-items: stretch;
  align-items: start;
  grid-auto-flow: row;
  grid-auto-columns: 1fr;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto;
  column-gap: 2rem;
  row-gap: 2rem;
}
</style>