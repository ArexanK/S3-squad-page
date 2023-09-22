<script>
  /** @type {import("@prismicio/client").Content.MainSlice} */
  export let slice;
  console.log(slice.items[0].linksquads)
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
<div class="fdnd-squadpage">
  <div class="plates">
    <div class="sparkles-top">
      <div class="sparkle1"></div>
      <div class="sparkle2"></div>
      <div class="sparkle3"></div>
    </div>
    <div class="h1-center">
    <h1>{slice.items[0].title}</h1>
    </div>
    <div class="plate"></div>
    <div class="front-plate"></div>

    <div class="sparkles-bottom">
      <div class="sparkle-bottom1"></div>
      <div class="sparkle-bottom2"></div>
    </div>
  </div>

  <div class="h2-center">
    <h2>Tribe</h2>
  </div>
  

  <div class="big-triangle">
    <svg height="100" width="400">
      <polygon points="200,1 350,100 50,100" style="fill: #D399BC; stroke: none; stroke-width:1"></polygon>
    </svg>
  </div>
  
  <div class="scribble">  
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 10">
      <path d="m 0 0
    l 10 10
    10 -10
    10 10
    10 -10
    10 10" 
    stroke="#FFCC10" stroke-width="2" fill="none"/>
    </svg>
  </div> 

  <div class="button">
    <a href="squadselect">Bezoek de squads</a>
  </div>

</section>

<style>
:root {
  --deep-blue: #55B6AE;
  --yellow: #FFCC10;
  --pinkish: #D399BC;
  --hot-pink: #FF3394;
  --light-blue: #90DCFF;
  --dark-blue: #5968A3;

}

/* Fdnd Squadpage */

.fdnd-squadpage {
  margin-top: 100px;
  width: 100%;
  height: 100%;
}

.fdnd-squadpage h1 {
  font-family: 'Quantico', sans-serif;
  text-transform: uppercase;
  color: white;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: black;
  transform: skew(-20deg) rotatez(2deg);
  text-align: center;
  margin-top: 21px;
  margin-left: 18px;
  position: absolute;
  z-index: 100;
  font-size: 45px;
  text-shadow: 5px 1px var(--hot-pink);
  max-width: 320px;
}

.plate {
  background-color: var(--deep-blue);
  margin: auto;
  width: 85%;
  height: 110px;
  transform: skew(-15deg) rotateX(15deg) rotateY(-175deg);
  position: relative;
  z-index: 5;
}

.front-plate {
  background-color: var(--yellow);
  margin: -50px auto;
  width: 85%;
  height: 110px;
  transform: skew(-15deg) rotateX(15deg) rotateY(-173deg);
  position: relative;
  z-index: 10;
}

.h2-center {
  justify-content: center;
  display: flex;
}

.fdnd-squadpage h2 {
  font-family: 'Knewave', cursive;
  text-transform: uppercase;
  color: var(--light-blue);
  font-size: 80px;
  position: absolute;
  z-index: 20;
  transform: rotate(20deg);
  letter-spacing: 10px;
  text-shadow: 6px 3px black;
  margin-top: 30px;
  margin-left: 20px;
}

.big-triangle {
  margin-top: 24px;
  rotate: 17deg;
}

.button {
  margin: auto;
}

a {
  background-color: var(--deep-blue);
  border-radius: 6px;
  padding: 20px;
  font-size: 20px;
  color: white;
  text-decoration: none;
}

/* Decorations */

.sparkles-top {
  position: absolute;
  right: 40px;
  rotate: -47deg;
  z-index: 30;
}

.sparkle1 {
  background-color: var(--hot-pink);
  width: 20px;
  height: 20px;
}

.sparkle2 {
  background-color: var(--yellow);
  width: 30px;
  height: 30px;
  transform: translate(40px, -16px);
}

.sparkle3 {
  background-color: var(--yellow);
  width: 20px;
  height: 20px;
  transform: translate(7px, -1px);
}

.sparkles-bottom {
  position: absolute;
  margin-top: 40px;
  rotate: 3deg;
  z-index: 30;
}

.sparkle-bottom1 {
  background-color: var(--hot-pink);
  width: 25px;
  height: 25px;
  rotate: 75deg;
}

.sparkle-bottom2 {
  background-color: var(--yellow);
  width: 30px;
  height: 30px;
  transform: rotate(15deg) translate(40px, -16px);
}

.scribble {
  position: relative;
  z-index: 10;
  width: 100px;
  rotate: 30deg;
}

.scribble svg {
  filter: drop-shadow(1px 3px 0px black);
}

.button {
  margin-top: 60px;
  display: flex;
  justify-content: center;
}


/* Desktops and laptops */
@media only screen 
and (min-width : 750px) {

  .fdnd-squadpage h1 {
    max-width: 510px;
    font-size: 70px;
    margin-top: -40px;
  }

  .h1-center {
    display: flex;
    justify-content: center;
  }

  .big-triangle {
    margin: 10px auto;
    border-width: 0 397px 286px 347px;
    transform: rotate(7deg);
    width: 310px;
}

  .sparkles-top {
    margin-right: 60px;
  }

  .scribble {
    margin-top: 0px;
    margin-left: 260px;
  }

}
</style>