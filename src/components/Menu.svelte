<script>
  import { Router, Link } from 'svelte-routing';
  import { fly, scale } from 'svelte/transition';
  import { quadOut } from 'svelte/easing';

  export let open;
</script>

{#if open}
  <nav class='bg-white-900 font-bold' on:click={ () => open=false }>
    <Router>
      <Link class='block text-sm p-4' to="/">Home</Link>
      <div class='bar' transition:scale={{ duration: 200, easing: quadOut, opacity: 1 }} />
      <Link class='block text-sm p-4' to="about">フタリゴトとは？</Link>
      <div class='bar' transition:scale={{ duration: 200, easing: quadOut, opacity: 1, delay: 100 }} />
      <Link class='block text-sm p-4' to="episodes">エピソード</Link>
      <div class='bar' transition:scale={{ duration: 200, easing: quadOut, opacity: 1, delay: 200 }} />
    </Router>
  </nav>
{/if}

<style>
    nav {
        text-align: center;
        font-size: 1.5em;
        letter-spacing: 0.15em;
        padding: 1em;
        padding-top: 0;
        color: #FFA45B;
    }
    a {
        cursor: pointer;
        width: max-content;
        margin: 1rem auto;
        display: block;
    }
    .bar {
        margin: 0 auto;
        width: 75%;
        border-style: solid;
        border-color: #FFA45B;
        border-width: 0.5px;
        height: 0;
    }
</style>
