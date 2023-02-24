<script lang="ts">
  import Button from "$lib/Button.svelte";
  import KofiLogo from "$lib/Icons/KofiLogo.svelte";
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
      <Button text="services" link="/" />
      <Button text="premade shop" icon={KofiLogo} style="outlined"  link="https://ko-fi.com/mattsquare" />
    </div>
  </div>
</div>

<style>

</style>