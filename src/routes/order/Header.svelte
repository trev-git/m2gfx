<script>
  export let icon;
  export let text;
</script>

<div class="header">
  <div class="icon">
    <svelte:component this={icon} weight={"fill"} color={"#5ee2bb"} size={24}/>
  </div>
  <h3 class="text">{text}</h3>
</div>

<style>
  .header {
    display: flex;
    align-items: center;
    font-family: "Poppins";
    font-weight: 900;
    margin-bottom: 1rem;
  }
  .icon {
    margin-right: 1rem;
  }
  .text {
    margin: 0;
    color: #5ee2bb;
  }
</style>