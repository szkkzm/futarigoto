<script>
import { onMount } from 'svelte';
import { guestList } from '../guest-list';

onMount(()=>{
  window.scrollTo(0,0);
})
</script>
<h3 class='text-base sm:text-xl text-accent-500 my-5 sm:mt-10'>ABOUT "FUTARIGOTO" </h3>
<img src="/about_page.jpg" alt="フタリゴトとは？のトップ画像" class='px-8'/>

<div class='mx-8 text-left sm:text-center '>
  <p class='text-xl text-primary-500 font-bold pt-5 sm:text-2xl'>変化の時代、<br>
    本当に必要なコトは、<br>
    対話によって得られる。
  </p>
  <p class='text-sm text-primary-400 my-8'>
    フタリゴトでは、現代で活躍する現役高専生や高専卒の方をお招きし、高専とは何か？そこで形づくられた自分とは何か？について対話します。<br>
    <br>
    ゲストの方から見た高専像、自らの生き方を決めたプロセスが、やりたいことを見つめ直すきっかけになれば幸いです。
  </p>
</div>
<h3 class='text-base sm:text-xl text-accent-500 my-5 sm:mt-10'>CAST & STAFF</h3>

<div class='bg-white-900 mx-8 sm:mx-60'>
  <h3 class='text-base text-accent-500 pt-3'>GUEST</h3>
  <div class='text-left px-3 '>
    {#each guestList as gl}
      <div class='text-left px-3 py-6 sm:text-center'>
        <p class='font-bold'>{ gl.name }</p>
        <p class='text-xs'>{@html gl.text}</p>
      </div>
    {/each}
  </div>
</div>

<div class='bg-white-900 mx-8 mt-8 sm:mx-60'>
  <h3 class='text-base text-accent-500 pt-3'>MODERATOR</h3>
  <div class='text-left px-3'>
    <div class='text-left px-3 py-6 sm:text-center'>
      <p class='font-bold'>関戸大</p>
      <p class='text-xs'>株式会社bokutaku代表取締役<br>日本を変える学校を創るべく活動中。</p>
    </div>
  </div>
</div>

<div class='bg-white-900 mx-8 my-8 sm:mx-60'>
  <h3 class='text-base text-accent-500 pt-3'>CAMERAMAN & EDITOR</h3>
  <p class='text-left px-6 py-3 font-bold sm:text-center'>Kzm.</p>
</div>


<style>
  @font-face{font-family: Senobi-Gothic;
  src: url(/Senobi-Gothic-Regular2.woff2);}
  h2 {
    font-family: Senobi-Gothic;
    letter-spacing: 0.05rem;
  }
  h3{
    font-family: Futura;
    letter-spacing: 0.2rem;
  }
</style>
