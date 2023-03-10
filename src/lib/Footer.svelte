<script lang="ts">
  import LogoSmall from "$lib/Icons/LogoSmall.svelte";
  import KofiLogo from "$lib/Icons/KofiLogo.svelte";
  import { TwitterLogo, FileCode, ClipboardText } from "phosphor-svelte";
  import FooterButton from "$lib/FooterButton.svelte";
  
  const logoLink: string = '/';
</script>

<footer class="footer">
  <div class="wrapper footer-wrapper">
    <div class="space-between">
      <a class="footer-logo-link" href={logoLink}>
        <LogoSmall size="4rem" />
        <p class="button-text">&copy; 2023</p>
      </a>
      <div class="footer-logo-small-links">
          <FooterButton icon={TwitterLogo} link="https://twitter.com/mattsquare_" newTab={true} />
          <FooterButton icon={KofiLogo} link="https://ko-fi.com/mattsquare" />
      </div>
    </div>
    <div class="_2rem-layout">
      <div class="footer-small-links">
        <FooterButton icon={TwitterLogo} link="https://twitter.com/mattsquare_" newTab={true} />
        <FooterButton icon={KofiLogo} link="https://ko-fi.com/mattsquare" newTab={true} />
      </div>
      <FooterButton icon={FileCode} text="coded by trev" link="https://trev-git.github.io/professional-kelp/" newTab={true} />
      <FooterButton icon={ClipboardText} text="read terms" link="/terms" />
    </div>
  </div>
</footer>

<style>
  footer.footer {
    width: 100vw;
    max-width: 100%;
    position: absolute;
    bottom: 0;
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
    padding-block: 2rem;
    padding-inline: 4rem;
    column-gap: 4rem;
    row-gap: 4rem;
    -webkit-transition: background-color .2s ease;
    transition: background-color .2s ease;
  }

  footer.footer:hover {
    background-color: var(--secondary-two-32);
  }

  .wrapper.footer-wrapper {
    -webkit-box-pack: start;
    -webkit-justify-content: flex-start;
    -ms-flex-pack: start;
    justify-content: flex-start;
    column-gap: 4rem;
    row-gap: 4rem;
  }

  .footer-logo-link {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    column-gap: 1.5rem;
    row-gap: 1.5rem;
    opacity: 0.3;
    -webkit-transition: opacity .2s ease;
    transition: opacity .2s ease;
  }

  .footer-logo-link:hover {
    opacity: 1;
  }

  .footer-logo-small-links {
    display: none;
    opacity: 0.3;
  }

  .footer-small-links {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;

  }
</style>