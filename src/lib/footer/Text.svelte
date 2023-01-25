<script>
  export let text;
</script>

<div class="text">
  <p>{text}</p>
</div>

<style>
  p {
    color: #fff;
    font-family: "Poppins";
    font-style: normal;
    font-weight: 700;
    font-size: 12px;
    margin: 0;
  }
  .text {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin: 0 1rem;
  }
</style>