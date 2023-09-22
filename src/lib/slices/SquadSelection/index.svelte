<script>
  /** @type {import("@prismicio/client").Content.SquadSelectionSlice} */
  export let slice;
  console.log(slice);
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  <section class="title">
    <h1>{slice.primary.title}</h1>
  </section>
    <div class="plate" />
    <div class="front-plate" />
  </section>
  <section class="subtitle">
    <p>{slice.primary.subtitle}</p>
    <div class="zigzag">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 10">
        <path
          d="m 0 0
      l 10 10
      10 -10
      10 10
      10 -10
      10 10
      10 -10
      "
          stroke="#90dcff"
          stroke-width="3"
          fill="none"
        />
      </svg>
    </div>
  </section>

  <div class="button-wrapper">
    <section class="button-a">
      <a href=/squad-leden/squadA>
        <span class="first-word">Squad</span>
        <span class="second-word">A</span></a
      >
    </section>
    <section class="button-b">
      <a href=/squad-leden/squadB
        ><span class="first-word">Squad</span>
        <span class="second-word">B</span></a
      >
    </section>
  </div>

<style>
  * {
    box-sizing: border-box;
    margin: 0px;
    line-height: 1.4;
  }


  :root {
    --deep-blue: #55b6ae;
    --blue-purple: #768bba;
    --pinkish: #d399bc;
    --hot-pink: #ff3394;
    --light-blue: #90dcff;
  }

  /* main {
    margin-top: 100px;
    width: 100%;
    height: 100%;
    margin-left: 10px;
  } */
  /*section title*/
  h1 {
    font-family: "Quantico", sans-serif;
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
    font-size: 50px;
    text-shadow: 5px 1px var(--hot-pink);
  }

  .first-word {
    font-family: "Quantico", sans-serif;
    text-transform: uppercase;
    color: white;
    font-size: 20px;
    font-weight:300;
   
  }

  .second-word {
    color: var(--light-blue);
    font-size: 50px;
  }

  .plate {
    background-color: var(--pinkish);
    margin: auto;
    width: 95%;
    height: 110px;
    transform: skew(-15deg) rotateX(15deg) rotateY(-175deg);
    position: relative;
    z-index: 5;
  }

  .front-plate {
    background-color: var(--deep-blue);
    margin: -50px auto;
    width: 95%;
    height: 110px;
    transform: skew(-15deg) rotateX(15deg) rotateY(-173deg);
    position: relative;
    z-index: 10;
  }

  /*end section title*/

  /*section subtitle*/
  .subtitle {
    font-family: "Quantico", sans-serif;
    font-size: 30px;
    font-weight: bold;
    text-transform: uppercase;
    color: var(--blue-purple);
    text-align: center;
    margin-top: 120px;

  }

  /*end section subtitle*/

  /* section buttons*/

  a {
    margin: 0;
    height: 100dvh;
    display: grid;
    place-items: center;
    text-decoration: none;

    aspect-ratio: 1;
    height: 6.5em;
    background-color: var(--pinkish);
    transform: skewX(20deg);
    box-shadow: -1em 1em 0 var(--blue-purple);
    border-radius: 0.5em;
    transition: 0.5s;

    font-family: "Quantico", sans-serif;
    text-transform: uppercase;
    color: white;
    -webkit-text-stroke-width: 2px;
    -webkit-text-stroke-color: rgb(255, 255, 255);
  }

  a:hover {
    transform: skewX(-20deg);
    box-shadow: 1em 1em 0 var(--blue-purple);
  }

  .button-wrapper {
    display: flex;
    justify-content: space-evenly;
    margin-top: 5%;
  }

  /* end section buttons*/

  /* figuurtjes*/

  .zigzag {
    /* position: relative; */
    z-index: 20;
    width: 100px;
    /* rotate: 10deg; */
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 30px auto;
  }

  /* Desktops and laptops */
  @media only screen and (min-width: 750px) {

    .title {
      display: flex;
      justify-content: center;
    }
    .title h1 {
      max-width: 510px;
      font-size: 70px;
      margin-top: -40px;
    }
    .zigzag {
    
      margin:30px auto;
    }
  }
</style>
