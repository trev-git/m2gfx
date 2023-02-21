<script lang="ts">
  import LogoSmall from "$lib/Icons/LogoSmall.svelte"
  import NavButton from "$lib/NavButton.svelte";

  const logoLink: string = '/';
  const navButtons: {text: string, style: string, link: string}[] = [
    {
      text: 'home',
      style: '',
      link: '/'
    },
    {
      text: 'donate',
      style: '',
      link: 'https://ko-fi.com/mattsquare'
    },
    {
      text: 'works',
      style: '',
      link: '/works'
    },
    {
      text: 'contact',
      style: '',
      link: '/contact'
    },
    {
      text: 'order',
      style: 'active',
      link: '/order'
    }
  ]
</script>

<nav class="nav-bar">
  <div class="wrapper">
    <a class="logo" href={logoLink}>
      <LogoSmall size="5rem"/>
    </a>
    <div class="_2rem-layout nav-links">
      {#each navButtons as button}
        <NavButton text={button.text} style={button.style} link={button.link} />
      {/each}
    </div>
  </div>
</nav>

<style>
  nav.nav-bar {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -webkit-justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    position: fixed;
    padding-block: 2rem;
    padding-inline: 4rem;
    width: 100vw;
    max-width: 100%;
    z-index: 1000;
    background-image: -webkit-gradient(linear, left top, left bottom, from(#000), to(transparent));
    background-image: linear-gradient(180deg #000 transparent);
  }

  .logo {
    -webkit-transition: -webkit-transform .2s ease;
    transition: transform .2s ease, -webkit-transform .2s ease;
    color: green;
  }

  .logo:hover {
    -webkit-transform: scale(1.1);
    -ms-transform: scale(1.1);
    transform: scale(1.1);
  }
</style>
