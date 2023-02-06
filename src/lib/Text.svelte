<script lang="ts">
  export let text: string;
  export let href: string | null = null;
  export let icon: any = null;
</script>

<a class="text" {href}>
  <svelte:component this={icon} weight={"fill"}/>
  <p>{text}</p>
</a>

<style>
  a {
    all: unset;
    display: inline-flex;
    align-items: center;
    color: #fff;
    font-family: "Poppins";
    font-style: normal;
    font-weight: 700;
    margin: 0;
    gap: 1rem;
    cursor: pointer;
  }
  p {
    margin: 0;
  }
  .text {
    opacity: 0.3;
    transition: 300ms;
    font-size: 1.5rem;
  }
  .text:hover {
    transition: 300ms;
    opacity: 1;
  }
</style>