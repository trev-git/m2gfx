<script lang="ts">
  import MetaTitle from "$lib/MetaTitle.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    let contents = document.querySelectorAll('.content');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          const target = entry.target as HTMLElement;
          console.log(target);
          target.style.opacity = '1';
        }
      });
    });
    for (const content of contents) {
      observer.observe(content);
    }
  });
</script>

<MetaTitle title="Works" />

<style>
  
</style>