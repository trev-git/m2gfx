<script>
  import Button from "../Button.svelte";
  import Picture from "./Picture.svelte";
</script>

<div class="content">
  <div class="view">
    <p class="text">View some of my work:</p>
    <a href="#" class="btn">View more</a>
  </div>
  <div class="grid">
    <div class="left-grid">
      <div class="grid1">
        <Picture src={"Gaming_Overlay_Preview.png"} alt={"img"}/>
      </div>
      <div class="grid2">
        <Picture src={"Gaming_Overlay_Preview.png"} alt={"img"}/>
      </div>
      <div class="grid3">
        <Picture src={"Gaming_Overlay_Preview.png"} alt={"img"}/>
      </div>
    </div>
    <div class="right-grid">
      <div class="grid4">
        <Picture src={"Gaming_Overlay_Preview.png"} alt={"img"}/>
      </div>
      <div class="grid5">
        <Picture src={"Gaming_Overlay_Preview.png"} alt={"img"}/>
      </div>
      <div class="grid6">
        <Picture src={"Gaming_Overlay_Preview.png"} alt={"img"}/>
      </div>
    </div>
  </div>
  <div class="view">
    <p class="text">Are you interested in getting something for yourself?</p>
  </div>
  <Button text={"commision from me"}/>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;700&display=swap');
  .content {
    padding: 0 100px;
    margin: 4rem 0;
    font-family: "Poppins";
    font-weight: 700;
  }
  .view {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
  }
  .text {
    margin: 0;
  }
  .btn {
    all: unset;
    font-weight: 500;
    cursor: pointer;
    padding: 0.25rem 1rem;
    background-color: white;
    color: black;
    border-radius: 200px;
  }
  .grid {
    display: grid;
    grid-template-columns: 2.5fr 2fr;
    grid-auto-rows: min-content;
    gap: 1rem;
    margin-bottom: 4rem;
  }
  .left-grid {
    display: grid;
    grid-template-columns: repeat(2, 1.25fr);
    grid-auto-rows: min-content;
    grid-column: 1;
    gap: 1rem;
  }
  .right-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-auto-rows: min-content;
    grid-column: 2;
  }
  .grid1 {
    grid-column: 1 / 3;
    grid-row: 1 / 3;
  }
  .grid2 {
    grid-column: 1;
    grid-row: 3;
  }
  .grid3 {
    grid-column: 2;
    grid-row: 3;
  }
  .right-grid {
    gap: 1rem;
  }
  .grid4 {
    grid-column: 1;
    grid-row: 1;
  }
  .grid5 {
    grid-column: 2;
    grid-row: 1;
  }
  .grid6 {
    grid-column: 1 / 3;
    grid-row: 2 / 3;
  }
</style>
