<script>
  /** @type {import("@prismicio/client").Content.SquadMembersSlice} */
  export let slice;
  import { PrismicImage } from '@prismicio/svelte'

</script>

<section
  data-slice-type={slice.slice_type}
  data-slice-variation={slice.variation}
>
<ul>
  {#each slice.items as item}
    <li>
      <div class="imgBorder">
        <PrismicImage field={item.memberdata.data.memberimg} width="140" height="140"/>
      </div>
      <h2>Naam: {item.memberdata.data.membername}</h2>
      <span>Squad: {item.memberdata.data.squadname}</span>
      <a href="{item.memberdata.data.githublink.url}">Github Link</a>
    </li>
  {/each}
</ul>
</section>

<style>
  /* Style for the profile cards */
  ul {
    list-style: none;
    padding: 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  li {
    background-color: #ffffff;
    border: 1px solid #eaeaea;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    margin: 10px;
    width: calc(33.33% - 20px);
    text-align: center;
    transition: transform 0.3s ease-in-out;
  }

  li:hover {
    transform: translateY(-5px);
  }

  h2 {
    font-size: 1.5rem;
    margin: 10px 0;
  }

  span {
    display: block;
    margin: 5px 0;
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
    margin: 10px 0;
  }

  /* Responsive styles */
  @media screen and (max-width: 768px) {
    li {
      width: 100%;
    }
  }
</style>
