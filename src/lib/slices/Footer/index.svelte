<script>
  /** @type {import("@prismicio/client").Content.FooterSlice} */
  import { PrismicImage } from '@prismicio/svelte'
  export let slice;

  // console.log(slice.items[0].hvalogo);

</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
  
  <footer>
    <img class="hva-logo" src="{slice.items[0].hvalogo.url}" alt="hva logo"/>
    <span> © 2023 FDND Squadpage </span>
  </footer>

</section>

<style>

  :root {
    --white: #fff;
    --turquoise: #55B6AE;
  }

  footer{
    background-color: var(--turquoise);
    width: 100%;
    height: auto;
    margin-top: 2em;
    position: sticky;
    bottom: 0;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .hva-logo{
    max-width: 85%;
    height: auto;
  }

  span{
    color: var(--white);
    font-size: .7em;
    padding: 1em;
  }

  @media (min-width: 400px) {

    .hva-logo{
    width: 15rem;
    }
  }

  @media (min-width: 800px) {

    footer{
      flex-direction: row;
      justify-content: space-between;
    }
    .hva-logo{
    width: 20rem;
    }
    
    .hva-logo{
    width: 20rem;
    }

  }
</style>