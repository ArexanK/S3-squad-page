<script>
  /** @type {import("@prismicio/client").Content.HeaderSlice} */
  export let slice;
  // console.log(slice.items[0])
</script>


<header>
  <h1 class="fdnd"><a href="/">fdnd</a></h1>
  <a href={slice.items[0].overons.url}>Over ons</a>
</header>


<style>
  :root {
    --white: #fff;
    --turquoise: #55B6AE;
    --rounded: .3rem;
    --shadow: .3rem
  }
    
  header {
    background-color: #ffffff;
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
  }

  .fdnd a {
    font-size: 1.2rem;
    border: 1px solid var(--white);
    border-radius: var(--rounded);
    color: var(--white);
    background: var(--turquoise);
    text-transform: lowercase;
    padding: 0.5rem 1.2rem;
    display: block;
  }

  .fdnd a:hover {
    text-decoration: none;
  }

  a {
    text-decoration: none;
    color: var(--turquoise);
    text-transform: uppercase;
    font-family: 'Quantico', openSans, sans-serif;
    font-size: 1em;
    font-weight: bold;
  }

  a:hover{
    text-decoration: underline;
  }

  @media (min-width: 400px) {

    .fdnd {
      font-size: 1.4rem;
    }

    a {
      font-size: 1.2em;
    }
  }

  @media (min-width: 800px) {

    header{
      padding: 23px;
    }

    .fdnd {
      font-size: 2rem;
    }

    a {
      font-size: 1.5em;
    }
  }

</style>
