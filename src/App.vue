<template>
  <div>
    <section class="blue">
      <h1>Plamen Nanev presents: </h1>
      <p>The curvaceous site built with Vue and some CSS magic</p>
      <div class="curve"/>
    </section>

    <section>
      <h1>What does this showcase?</h1>
      <p>My skills with Vue and CSS, mostly just having fun and having something cool to look at</p>
    </section>
    <section class="bubble">
      <h1>Pretty cool, huh?</h1>
      <p>I've got more skills under my belt. Such as:</p>
    </section>
    <section class="dark">
      <h1>Java, Python, Docker, AWS, Prefect, JS, Node.JS and many more!</h1>
      <p>I wouldn't have enough space if I had to list them all!</p>
    </section>
    <section class="red">
      <h1>This couldn't been done without:</h1>
      <p>Youtube, CSS, KUBE.js, Haikei and Shape Divider</p>
      <div class="wave">
        <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
          <path
              d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
              class="shape-fill"></path>
        </svg>
      </div>
    </section>

    <div class="spacer layer1"/>

    <section>
      <h1>Please don't view this as something serious</h1>
      <p>This is something that I made to test some skills that I've learned from a YouTube video about creating waves with CSS.</p>
    </section>

    <div class="spacer layer2"/>

    <section class="pink">
      <h1>Of Course, I took it a step further</h1>
      <p>I decided to implement everything I learned in Vue and deploy it to the internet! Make it more shiny, put a better design and make it my own! The code will be made public when ready, alongside all scripts and files accompanying it </p>

      <svg
          id="visual"
          viewBox="0 0 960 400"
          width="960"
          height="400"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          version="1.1"
      >
        <g transform="translate(483.77650833544976 190.72725273656422)">
          <path
              id="blob1"
              d="M76.5 -95.1C99.5 -71.9 118.7 -48.1 132.4 -16.5C146.2 15.1 154.5 54.6 142.9 89.9C131.3 125.3 99.9 156.6 65.2 161.8C30.4 167 -7.5 146 -37.3 125.2C-67 104.5 -88.5 84 -111.3 57.8C-134.1 31.6 -158.1 -0.2 -155.8 -29.9C-153.4 -59.5 -124.6 -86.8 -94.2 -108.6C-63.9 -130.4 -31.9 -146.7 -2.6 -143.7C26.8 -140.6 53.6 -118.2 76.5 -95.1"
              fill="#BB004B"
          ></path>
        </g>
        <g
            transform="translate(475.51948293452494 185.87928222433226)"
            style="visibility: hidden"
        >
          <path
              id="blob2"
              d="M114.4 -128C143.2 -112.3 157.7 -71.3 154.4 -35.4C151 0.6 129.6 31.5 111.3 65.1C92.9 98.7 77.6 134.8 49.3 152.5C21.1 170.1 -20.1 169.1 -50.8 152.4C-81.5 135.6 -101.8 103.1 -117.9 70.4C-133.9 37.7 -145.7 5 -145.9 -31.2C-146 -67.3 -134.4 -106.8 -108.1 -123C-81.8 -139.2 -40.9 -132.1 1 -133.3C42.9 -134.4 85.7 -143.8 114.4 -128"
              fill="#BB004B"
          ></path>
        </g>
      </svg>
    </section>

    <div class="spacer layer2 flip"/>

    <section>
      <h1>Thank you for reading</h1>
      <p>This means a lot to me!</p>
      <p>Check me out on GitHub:</p>
      <img src="./assets/qr-code.svg" alt="nothing" >
    </section>
  </div>
</template>

<script>
import KUTE from 'kute.js'

export default {
  name: 'App',
  mounted() {
    this.animateBlob();
  },
  methods: {
    animateBlob() {
      console.log("I'm iiin")
      const tween = KUTE.fromTo(
          '#blob1',
          {path: '#blob1'},
          {path: '#blob2'},
          {repeat: 999, duration: 3000, yoyo: true},
      )
      tween.start()
    }
  }
}
</script>

<style>
h1 {
  font-size: 4rem;
}

p {
  font-size: 1.5rem;
}

body {
  margin: 0;
  font-family: "Prompt", sans-serif;
  color: white;
  background: #202731;
  overflow-x: hidden;
}

section {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 400px;
  padding: 100px 20vw;
}

.blue {
  background: #3c31dd;
}

.red {
  background: #c62368;
}

.pink {
  background: #f9046a;
}

.dark {
  background: #0f0f10;
}

.curve {
  position: absolute;
  height: 225px;
  width: 100%;
  bottom: 0;
}

.curve::before {
  content: "";
  display: block;
  position: absolute;
  border-radius: 100% 50%;
  width: 55%;
  height: 100%;
  background-color: #202731;
  transform: translate(85%, 60%);
}

.curve::after {
  content: "";
  display: block;
  position: absolute;
  border-radius: 100% 50%;
  width: 55%;
  height: 100%;
  background-color: #3c31dd;
  transform: translate(-4%, 40%);
  z-index: -1;
}

.bubble::after {
  content: "";
  border-top-left-radius: 50% 100%;
  border-top-right-radius: 50% 100%;
  position: absolute;
  bottom: 0;
  height: 85%;
  width: 100%;
  background-color: #0f0f10;
  z-index: -1;
}

.wave {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  line-height: 0;
}

.wave svg {
  position: relative;
  display: block;
  width: calc(100% + 1.3px);
  height: 215px;
}

.wave .shape-fill {
  fill: #0f0f10;
}

.spacer {
  aspect-ratio: 960/300;
  width: 100%;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.layer1 {
  background-image: url("./assets/waves/wave1.svg");
}

.layer2 {
  background-image: url("./assets/waves/wave2.svg");
}

.flip {
  transform: rotate(180deg);
}

.blob-motion {
  position: absolute;
  transform: translateY(-20%);
}

img {
  max-height: 250px;
  max-width: 250px;
}
</style>
