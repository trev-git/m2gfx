<script lang="ts">
export let imageSrc: string = '/Showcase Images/BRB Screen.png';

const mostX = 9;
const mostY = 9;

let width: number;
let height: number;

$: style = `transform: rotateY(0deg) rotateX(0deg);`;

// this is super laggy, it doesn't use much more cpu than the webflow site but it still is super slow
function rotateOnMouseOver (e: MouseEvent) {
  const x = e.offsetX;
  const y = e.offsetY;

  const halfWidth = width / 2;
  const halfHeight = height / 2;

  //calculate angle angles
  const rotationX = (((x - halfWidth) / halfWidth) * mostX).toFixed(4);
  const rotationY = (((y - halfHeight) / halfHeight) * mostY).toFixed(4);

  style = `transform: rotateY(${rotationY}deg) rotateX(${rotationX}deg`
}
</script>

<div class="showcase-container" on:mousemove={rotateOnMouseOver} bind:clientWidth={width} bind:clientHeight={height} style={style}>
  <div class="highlight"></div>
  <div class="shadow"></div>
  <img
    class="showcase-image"
    alt="Work Showcase"
    src={imageSrc}
  >
</div>

<style>
.showcase-container {
  position: relative;
  overflow: hidden;
  border-radius: 1rem;
  box-shadow: 0 16px 90px var(--secondary-two-32);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  -webkit-transform: perspective(800px);
  transform: perspective(800px);
  -webkit-transition: -webkit-transform .1s ease;
  transition: -webkit-transform .1s ease;
  transition: transform .1s ease;
  transition: transform .1s ease, -webkit-transform .1s ease;
}

.showcase-image {
  width: 100%;
}

.highlight {
  position: absolute;
  left: 0%;
  top: 0%;
  right: auto;
  bottom: auto;
  width: 75%;
  height: 125%;
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
  height: 125%;
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