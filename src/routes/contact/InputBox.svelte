<script lang="ts">
  export let placeholder: string = "Placeholder text";
  export let multiline: boolean = false;
  export let type: string = "text";
  export let label: string;
</script>

<div class="input-box">
  <label for="subject" class="bold-text">{label}</label>
  {#if !multiline}
    <input {type} {placeholder} class="normal-text" required>
  {:else}
  <div class="wrap">
    <img src="DotsSix.svg" alt="resize grabber"/>
    <textarea {placeholder} class="normal-text" rows="5" required></textarea>
  </div>
  {/if}
</div>

<style>
  .input-box {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  input, textarea {
    width: 100%;
    padding: 1rem 1.5rem;
    background: rgba(0, 0, 0, 0.32);
    border: 4px solid rgba(245, 245, 245, 0.32);
    border-radius: 16px;
    color: white;
    transition: border .2s ease-in-out;
  }
  input:invalid:not(:placeholder-shown) {
    border: 4px solid var(--accent);
  }
  input:valid, textarea:valid {
    border: 4px solid var(--accent-two);
    transition: border .2s ease-in-out;
  }
  textarea {
    resize: vertical;
    max-height: 1000px;
  }
  .wrap {
    position: relative;
  }
  img {
    position: absolute;
    right: 8px;
    bottom: 4px;
    pointer-events: none;
    z-index: 1;
  }
  ::-webkit-resizer {
    display: none;
  }
</style>