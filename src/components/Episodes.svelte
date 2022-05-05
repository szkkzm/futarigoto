<script>
  import { Button } from 'smelte';
  import { onMount } from 'svelte';
  import { movieList } from '../movie-list';

  onMount(()=>{
    window.scrollTo(0,0);
  })

</script>

<h3 class='text-base sm:text-xl text-accent-500 my-5 sm:mt-10'>EPISODE LIST </h3>

<div class='sm:flex pt-0'>
  {#each movieList as ml}
    <div class='bgHover shadowDiv mx-12 mb-12 bg-white-900 sm:w-80 sm:m-6' >
      <h3 class='text-base text-primary-300 py-2'>{ ml.title }</h3>
      <img class='sm:w-80' src={ ml.img } alt="サムネイル画像"/>
      <h3 class='text-accent-500 text-sm my-3'>{ ml.at }</h3>
      <p class='text-primary-900 text-xs pb-3 px-3 sm:text-sm'>{ @html ml.subTitle }</p>
      <div class='h-44 sm:block'>
        {#each ml.sections as s}
          <a href={ s.URL } target="_blank" rel="noopener noreferrer">
            <Button class='m-2 w-48' color="primary" light outlined>{ s.buttonText }</Button>
          </a>
        {/each}
      </div>
    </div>
  {/each}
</div>

<style>
.shadowDiv{
  filter: drop-shadow(5px 5px 5px #DDDDDD);
}
h3{
  font-family: Futura;
  letter-spacing: 0.2rem;
}
</style>
