<script>
      export let data;
      import { PrismicImage } from '@prismicio/svelte'
      import { SliceZone } from '@prismicio/svelte';
    import {components} from '$lib/slices'

    let backgroundTest = data.document.data.backgroundimg.url;
  </script>

<!-- {#each data.document as item}
<h1>{item.data.membername}</h1>
<h2>{item.data.squadname}</h2>
<a href={item.data.githublink.url}>Link</a>
<PrismicImage field={item.data.memberimg} />

{/each}

<SliceZone slices={data.slices} {components} />
{console.log(data)} -->


  <section class="wrapper" style="background-image: url({data.document.data.backgroundimg.url})">
    <!-- <PrismicImage field={data.document.data.backgroundimg} width="600"/>  -->
    <section class="core"> 
      <SliceZone slices={data.document.data.slices} {components} />
      <div class="sparkles-top">
        <div class="sparkle1"></div>
        <div class="sparkle2"></div>
        <div class="sparkle3"></div>
      </div>

      <div class="sparkles-bottom">
        <div class="sparkle-bottom1"></div>
        <div class="sparkle-bottom2"></div>
      </div>
    </section>
  </section>

<!-- {console.log(data)} -->

<style>

  .wrapper{
    position: absolute;
    height: 100%;
    width: 100%;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center;
    justify-content: center;
    background-size: 80% 100%;
  }

  .core{
    z-index: 6;
  }

  .sparkles-top {
  position: absolute;
  left: 2%;
  top: 10em;
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
  right: 5%;
  bottom: 6em;
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
</style>