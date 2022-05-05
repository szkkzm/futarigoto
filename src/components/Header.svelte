<script>
 import { Router, Link } from 'svelte-routing';
 import { Hamburger } from 'svelte-hamburgers';
 import Menu from './Menu.svelte';
 let open;
</script>

<header class='bg-white-900 text-dark-900 font-bold text-sm h-14'>
  <span class='sm:hidden flex justify-start'><Hamburger  bind:open --color='#FFA45B' type='elastic'/></span>
  <nav class='pt-4 invisible sm:visible flex justify-end'>
  	<Router>
      <span class='pr-16 linkHover'><Link to="/">Home</Link></span>
      <span class='pr-16 linkHover'><Link to="about">フタリゴトとは？</Link></span>
      <span class='pr-16 linkHover'><Link to="episodes">エピソード</Link></span>
    </Router>
  </nav>
</header>
<Menu bind:open />

<style>
  .linkHover:hover {
      color: #FFA45B;
      transition: color 0.2s linear;
  }
</style>
