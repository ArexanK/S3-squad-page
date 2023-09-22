<script>
  /** @type {import("@prismicio/client").Content.MainOveronsSlice} */
  export let slice;
  import { PrismicImage } from '@prismicio/svelte'
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
<!-- {console.log(slice.primary[1].title)}  -->

  <header>
    <h1> {slice.primary.title}</h1>
    <div class="plate"/>
    <div class="front-plate"/>
  </header>

  <article>
    <h2> {slice.primary.subtitle}</h2>
    <ul>
      <li>
        <PrismicImage field={slice.items[0].memberimg} width="70" height="100"/>
        <p>{slice.items[0].membername}</p>
        <a href="{slice.items[0].githublink.url}">Github</a>
      </li>
      <li>
        <PrismicImage field={slice.items[1].memberimg} width="70" height="100"/>
        <p>{slice.items[1].membername}</p>
        <a href="{slice.items[1].githublink.url}">Github</a>
      </li>
    </ul>
    <ul>
      <li>
        <PrismicImage field={slice.items[2].memberimg} width="70" height="100"/>
        <p>{slice.items[2].membername}</p>
        <a href="{slice.items[2].githublink.url}">Github</a>
      </li>
      <li>
        <PrismicImage field={slice.items[3].memberimg} width="70" height="100"/>
        <p>{slice.items[3].membername}</p>
        <a href="{slice.items[3].githublink.url}">Github</a>
      </li>
      <li>
        <PrismicImage field={slice.items[4].memberimg} width="70" height="100"/>
        <p>{slice.items[4].membername}</p>
        <a href="{slice.items[4].githublink.url}">Github</a>
      </li>
    </ul>
  </article>
</section>

<style>

  section{
    margin-top: 2em;
  }

  header{
    padding-bottom: 5em;
  }

  h1{
    text-transform: uppercase;
    color: white;
    -webkit-text-stroke-width: 2px;
    -webkit-text-stroke-color: black;
    transform: skew(-20deg) rotatez(2deg);
    text-align: center;
    margin-top: 1.7rem;
    margin-left: 3.1rem;
    position: absolute;
    z-index: 100;
    font-size: 3rem;
    text-shadow: 5px 1px var(--hot-pink);
  }

  .plate {
    background-color: #90DCFF;
    margin: auto;
    width: 95%;
    height: 5em;
    transform: skew(-15deg) rotateX(15deg) rotateY(-175deg);
    position: relative;
    z-index: 5;
  }

  .front-plate {
    background-color: var(--deep-blue);
    margin: -3rem auto;
    width: 95%;
    height: 5em;
    transform: skew(-15deg) rotateX(15deg) rotateY(-173deg);
    position: relative;
    z-index: 10;
  }

  h1, h2{
    font-family: 'Quantico', openSans, sans-serif;
  }

  h2{
    color: var(--deep-blue);
    text-align: center;
  }

  article{
    display: flex;
    flex-direction: column;
    width: 100%;
  }
  
  ul{
    display: flex;
    justify-content: center;
    list-style: none;
  }

  ul:nth-of-type(1){
    padding-top: 1.5em;
  }

  li{
    padding: .5em;
    width: 9em;
    margin: .5em;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    border: 2px solid var(--deep-blue);
    border-radius: 5px;
  }

  p{
    text-align: center;
  }

</style>