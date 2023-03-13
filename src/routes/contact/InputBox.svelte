<script lang="ts">
  import { DotsSix } from "phosphor-svelte";
import { onMount } from "svelte";

  export let placeholder: string = "Placeholder text";
  export let multiline: boolean = false;
  export let type: string = "text";
  export let label: string;
  export let required: boolean = false;

  let inputWidth: number;
  let inputHeight: number;
  let textareaWidth: number;
  let textareaHeight: number;

  $: spinSpeed = 1;
  $: spinOffset = 0;

  function generateLabel() {
    if (required) {
      return label + ' *';
    }

    else {
      return label
    }
  }

  onMount(() => {
    let frame = requestAnimationFrame(loop);

    function loop() {
      frame = requestAnimationFrame(loop);

      spinOffset = spinOffset - spinSpeed;
    }

    return (()=> {
      cancelAnimationFrame(frame);
    })
  })

  $: borderStyle = 'opacity: 0%;';

</script>

<div class="input-box">
  <label for="subject" class="bold-text">{generateLabel()}</label>
  
  {#if !multiline}
    <div class="input-wrapper" bind:clientWidth={inputWidth} bind:clientHeight={inputHeight}>
      <input
        {type}
        {placeholder}
        class="normal-text"
        {required}
        on:invalid={()=> {console.log('the form is invalid')}}
        on:focus={()=> {borderStyle = 'opacity: 100%';}}
        on:focusout={()=> {borderStyle = 'opacity: 0%';}}
      >
      <svg style={borderStyle} width={inputWidth} height={inputHeight} viewBox="0 0 {inputWidth} {inputHeight}" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="2" y="2" width={inputWidth - 4} height={inputHeight - 4} rx="16" stroke="currentColor" stroke-width="4" stroke-linecap="round" stroke-dasharray="110 10 36 10 8 10 34 10 143 10 18 10 54 10" stroke-dashoffset={spinOffset}/>
      </svg>
    </div>
  {:else}
    <div class="input-wrapper" bind:clientWidth={textareaWidth} bind:clientHeight={textareaHeight}>
      <div class="resize-dots">
        <DotsSix size="1.5rem" weight="bold" color="currentColor" />
      </div>
      <textarea
        {placeholder}
        class="normal-text"
        rows="5"
        required
        on:focus={()=> {borderStyle = 'opacity: 100%';}}
        on:focusout={()=> {borderStyle = 'opacity: 0%';}}
      ></textarea>
      <svg style={borderStyle} width={textareaWidth} height={textareaHeight} viewBox="0 0 {textareaWidth} {textareaHeight}" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="2" y="2" width={textareaWidth - 4} height={textareaHeight - 8} rx="16" stroke="currentColor" stroke-width="4" stroke-linecap="round" stroke-dasharray="110 10 36 10 8 10 34 10 143 10 18 10 54 10" stroke-dashoffset={spinOffset}/>
      </svg>
    </div>
  {/if}
</div>

<style>
  .input-box {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  
  .input-wrapper {
    position: relative;
  }

  svg {
    pointer-events: none;
    color: var(--accent-two);
    position: absolute;
    left: 0;
    top: 0;
    z-index: 1;
    transition: opacity .2s ease, color .2s ease;
  }

  input, textarea {
    width: 100%;
    padding: 1rem 1.5rem;
    background: var(--secondary-two-32);
    border: 4px solid var(--secondary-32);
    border-radius: 16px;
    color: white;
    transition: border .2s ease;
  }

  input:invalid:not(:placeholder-shown) {
    border-color: var(--accent);
    color: var(--accent);
  }

  input:invalid:not(:placeholder-shown) + svg {
    color: var(--accent);
  }

  input:focus, textarea:focus, input:invalid:focus, textarea:invalid:focus {
    border: 4px solid transparent;
    transition: border .2s ease;
  }

  textarea {
    resize: vertical;
    max-height: 1000px;
    min-height: 100px
  }

  .resize-dots {
    position: absolute;
    right: .5rem;
    bottom: .5rem;
    pointer-events: none;
    z-index: 1;
    opacity: 0.5;
  }
  
  ::-webkit-resizer {
    display: none;
  }
</style>