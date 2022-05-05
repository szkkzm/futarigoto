<script>
	export let url='';
	import "smelte/src/tailwind.css" ;
  import { Router, Link, Route } from "svelte-routing";
	import Header from './components/Header.svelte';
	import Footer from './components/Footer.svelte';
	import Home from './components/Home.svelte';
	import About from './components/About.svelte';
	import Episodes from './components/Episodes.svelte';
</script>

<main class='bg-background-900 text-primary-900'>
	<Header />
	<Router url="{url}">
	  <div>
	    <Route path="episodes" component="{Episodes}" />
	    <Route path="about" component="{About}" />
	    <Route path="/"><Home /></Route>
	  </div>
	</Router>
	<Footer />
</main>

<style>
	main {
		font-family: "游ゴシック体", YuGothic, "游ゴシック", "Yu Gothic", sans-serif;
		text-align: center;
		margin: 0 auto;
	}
</style>
