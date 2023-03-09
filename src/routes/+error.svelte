<script lang="ts">
  import { House } from "phosphor-svelte";
  import Button from "$lib/Button.svelte";
</script>

<div class="content">
  <div class="title-layout">
    <div class="title-text-layout">
      <h1 class="title">
        404. >->'<br>Not found 
      </h1>
      <p class="normal-text">
        Sorry to say that, even after searching far and wide and under every nook and cranny,
        we still couldn&#x27;t find what you were looking for.
      </p>
      <p class="normal-text">
        The page you were trying to access possibly doesn&#x27;t exist, or is still in the works, but thank you for your patience!
        In the meantime, you can visit the other parts of my site and access everything else from the home page.
      </p>
    </div>
    <Button text="go to home page" icon={House} style="secondary" link="/" />
  </div>
</div>