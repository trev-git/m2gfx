<script lang="ts">
  export let text: string = 'button text';
  export let style: '' | 'active' = '';
  export let link: string = '/';
</script>

<a class={"nav-button " + style} href={link}>
  <p class="button-text">{text}</p>
</a>

<style>
  .nav-button {
    padding-block: 0.5rem;
    padding-inline: 2rem;
    border-radius: 1000px;
    outline: solid 0.1rem transparent;
    -webkit-transition: .2s ease;
    transition: .2s ease;
  }

  .nav-button:hover {
    padding-inline: 3rem;
    outline-color: var(--accent-two);
    color: var(--accent-two);
  }

  .nav-button.active {
    outline: none;
    background-color: var(--secondary);
    color: var(--secondary-two);
  }

  .nav-button.active:hover {
    background-color: var(--accent-two);
    box-shadow: 0 2px 130px 0 var(--accent-two-50);
  }
</style>