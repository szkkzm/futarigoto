<script>
  import { onMount } from 'svelte';
  import Top from './Top.svelte';
  import { Button } from 'smelte';
  import { Router, Link } from 'svelte-routing';

  const toEisodesPage = () => {
    location.replace('./episodes');
  }
  onMount(()=>{
    window.scrollTo(0,0);
  })
</script>

<Top />
<h3 class='text-base sm:text-xl text-accent-500 my-5 sm:mt-10'>LATEST EPISODES</h3>
<a href="https://www.youtube.com/watch?v=bIWGe3s-cqc" target="_blank" rel="noopener noreferrer">
    <div class='bgHover shadowDiv mx-12 mb-12 bg-white-900 sm:w-3/5 sm:flex sm:mx-auto sm:my-8'>
      <img class='sm:h-48'src="/3-2.jpg" alt="サムネイル画像"/>
      <div class='sm:text-left'>
        <h3 class='text-accent-500 text-sm my-3 sm:text-base sm:pl-8'>2022/02/01</h3>
        <p class='text-primary-900 text-xs pb-3 sm:text-xl sm:font-bold sm:pl-8'>フタリゴト#3　辻貴美花×関戸大×佐々木尚</p>
        <p class='text-primary-900 text-xs pb-3 sm:text-sm sm:pl-8'>「高専発ベンチャーを経験した卒業生の話」【後編】</p>
      </div>
    </div>
  </a>

  <a href="https://www.youtube.com/watch?v=jn76fqIyFC0" target="_blank" rel="noopener noreferrer">
    <div class='bgHover shadowDiv mx-12 bg-white-900 sm:w-3/5 sm:flex sm:mx-auto sm:my-8'>
      <img class='sm:h-48'src="/3-1.jpg" alt="サムネイル画像"/>
      <div class='sm:text-left'>
        <h3 class='text-accent-500 text-sm my-3 sm:text-base sm:pl-8'>2022/02/01</h3>
        <p class='text-primary-900 text-xs pb-3 sm:text-xl sm:font-bold sm:pl-8'>フタリゴト#3　辻貴美花×関戸大×佐々木尚</p>
        <p class='text-primary-900 text-xs pb-3 sm:text-sm sm:pl-8'>「高専発ベンチャーを経験した卒業生の話」【前編】</p>
      </div>
    </div>
  </a>

<Router>
  <Link to="/episodes">
    <Button class='my-10 text-white-900 bg-accent-500'>すべてのエピソードを見る</Button>
  </Link>
</Router>

<style>
h3{
  font-family: Futura;
  letter-spacing: 0.2rem;
}
.shadowDiv{
  filter: drop-shadow(5px 5px 5px #DDDDDD);
}
.bgHover:hover {
  background-color: #CCCCCC;
  transition: background-color 0.2s linear;
}
</style>
