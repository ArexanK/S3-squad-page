<script>
  /** @type {import("@prismicio/client").Content.SquadMembersSlice} */
  export let slice;
  import { PrismicImage } from '@prismicio/svelte'
</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
<div>
  <h1>Squad {slice.items[0].memberdata.data.squadname}</h1>
  <div class="plate" />
  <div class="front-plate" />
</div>

<ul>
  {#each slice.items as item}
    <li>
      <a href="{item.memberdata.data.githublink.url}"><span class="imgBorder">      <h2>{item.memberdata.data.membername} </h2>
        <PrismicImage field={item.memberdata.data.memberimg} width="140" height="200"/></span>
      </a>
    </li>
  {/each}
</ul>
</section>

<style>
    div{
      margin-bottom: 6em;
      margin-top: -1.5em;
    }
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
    width: 100%;
  }

  .plate {
    background-color: var(--yellow);
    margin: auto;
    width: 85%;
    height: 110px;
    transform: skew(-15deg) rotateX(15deg) rotateY(-175deg);
    position: relative;
    z-index: 5;
  }

  .front-plate {
    background-color: var(--deep-blue);
    margin: -50px auto;
    width: 85%;
    height: 110px;
    transform: skew(-15deg) rotateX(15deg) rotateY(-173deg);
    position: relative;
    z-index: 10;
  }
  ul{
    display: flex;
    flex-flow: row wrap;
    gap: 1.5em;
    justify-content: center;
    width: 80%;
    height: 85%;
    transform: translateX(12.5%);

  }

  li {
    background-color: #ffffff;
    border: 1px solid #eaeaea;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    margin: 10px;
    width: calc(33.33% - 20px);
    text-align: center;
    margin-top: 10px;
  }
  h2{
    font-family: 'Quantico', sans-serif;
    color: var(--deep-blue);
    font-size: 25px;
    text-shadow: 2px 1px 2px rgb(135, 135, 135);
    height: 3em;

  }

  .imgBorder {
    border-radius: 50%;
    overflow: hidden;
    width: 140px;
    height: 140px;
    margin: 0 auto;
  }

  img {
    max-width: 100%;
    height: auto;
    display: block;
    transition: transform 0.3s ease-in-out;
  }

  img:hover {
    transform: scale(1.05);
  }

  a {
    text-decoration: none;
    color: #007bff;
    display: block;
    border: solid 4px rgb(110, 110, 110);
    padding: 1em;
    border-radius: 10px;
    background-color: white;
    box-shadow: 5px 2px 10px rgb(31, 30, 30);
    height: 20em;
  }
  a{
    text-decoration: none;
  }
</style>
