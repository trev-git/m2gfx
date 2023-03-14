<script lang="ts">
  export let imageSrc: string = '/Showcase Images/Oofu BRB Screen.png';

  let width: number;
  let height: number;
  let maxDegreeX = 30;
  let maxDegreeY = -18;

  $: style = `transform: rotateY(0deg) rotateX(0deg);`;
  $: highlightStyle = "left: 0%; top 0%;";
  $: shadowStyle = `left: 100%; top 0%;`;

  // this is super laggy, it doesn't use much more cpu than the webflow site but it still is super slow
  function rotateOnMouseOver(e: MouseEvent) {
    const { offsetX, offsetY } = e;

    const halfWidth = width / 2;
    const halfHeight = height / 2;

    const rotationX = (offsetX - halfWidth) / width * maxDegreeX;
    const rotationY = (offsetY - halfHeight) / height * maxDegreeY;

    style = `transform: perspective(5000px) rotateY(${rotationX}deg) rotateX(${rotationY}deg) scale(1.05)`;

    highlightStyle = `transform: translateX(${-(offsetX - halfWidth) / width * 100}%) translateY(${-(offsetY - halfHeight) / height * 100}%)`
    shadowStyle = `transform: translateX(${(offsetX - halfWidth) / width * 100}%) translateY(${(offsetY - halfHeight) / height * 100}%)`
  }

  function resetStyle() {
    style = `transform: perspective(5000px) rotateY(0deg) rotateX(0deg) scale(1)`
    highlightStyle = `transform: translateX(0) translateY(0)`;
    shadowStyle = `transform: translateX(0) translate(0)`;
  }
</script>

<div class="showcase-container" on:mousemove={rotateOnMouseOver} on:mouseleave={resetStyle} bind:clientWidth={width} bind:clientHeight={height} style={style}>
  <div class="highlight" style={highlightStyle}></div>
  <div class="shadow" style={shadowStyle}></div>
  <img
    class="showcase-image"
    alt="Work Showcase"
    src={imageSrc}
  >
</div>

<style>
.showcase-container {
  position: relative;
  border-radius: 1rem;
  box-shadow: 0 16px 90px var(--secondary-two-32);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  -webkit-transform: perspective(800px);
  transform: perspective(800px);
  -webkit-transition: -webkit-transform .15s ease;
  transition: -webkit-transform .15s ease;
  transition: transform .15s ease;
  transition: transform .15s ease, -webkit-transform .15s ease;
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
  will-change: transform;
}

img {
  width: 100%;
  height: 100%;
  border-radius: 1rem;
}

.highlight {
  position: absolute;
  left: 0%;
  top: 0%;
  right: auto;
  bottom: auto;
  width: 75%;
  height: 100%;
  border-radius: 50%;
  background-color: white;
  opacity: 0.12;
  -webkit-filter: blur(100px);
  filter: blur(100px);
  -webkit-transition: -webkit-transform .2s ease;
  transition: -webkit-transform .2s ease;
  transition: transform .2s ease;
  transition: transform .2s ease, -webkit-transform .2s ease;
}

.shadow {
  position: absolute;
  left: auto;
  top: auto;
  right: 0%;
  bottom: 0%;
  width: 75%;
  height: 100%;
  border-radius: 50%;
  background-color: black;
  opacity: 0.12;
  -webkit-filter: blur(100px);
  filter: blur(100px);
  -webkit-transition: -webkit-transform .2s ease;
  transition: -webkit-transform .2s ease;
  transition: transform .2s ease;
  transition: transform .2s ease, -webkit-transform .2s ease;
}
</style>