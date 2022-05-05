<script>
  import { Button } from 'smelte';
  import { Router, Link } from 'svelte-routing';
</script>

<div class='wrap'>
  <video src="movie_top.mp4" autoplay loop muted playsinline />
  <div class='cover'></div>
  <div class='title'>
    <h1 class='h4 pl-4 sm:pl-10'>フタリゴト</h1>
    <h2 class='h5 pl-5 sm:pl-14'>FUTARIGOTO</h2>
    <p class='text-xs pl-5 sm:pl-14'>「高専生とは何だろう？」<br>
      フタリゴトでは、現代で活躍する現役高専生や高専卒の方をお招きし、<br>
      高専についての情報をYoutubeにて発信しています。
    </p>
    <Router>
      <Link to="/about" class='pl-6 sm:pl-14'>
        <Button color="white" outlined class='mt-2 text-white-900 text-xs sm:text-sm sm:mt-6'>About "FUTARIGOTO" ≫</Button>
      </Link>
    </Router>
  </div>
</div>

<style>
  @font-face{font-family: Senobi-Gothic;
  src: url(/Senobi-Gothic-Regular2.woff2);}
  h1 {
    font-family: Senobi-Gothic;
    letter-spacing: 0.05rem;
  }
  h2{
    font-family: Futura;
    letter-spacing: 0.2rem;
  }
  .wrap {
  width:100vw;
  height: 56.25vw;
  position: relative;
  }
  video {
  width: 100%;
  }
  .cover {
  position: absolute;
  width:100vw;
  height: 56.25vw;
  top: 0;
  background-color: #999;

  opacity: 0.5;
  }

  .title{
  position: absolute;
  top: 5vw;
  color: #FFFFFF;
  text-shadow: 0px 0px 20px #FFA45B;
  text-align: left;
  }

  @media screen and (min-width: 640px) {
    h1 {
      font-size: 6rem;
    }
    h2 {
      font-size: 3rem;
      letter-spacing: 1rem;
    }
    p {
      font-size: 1rem;
    }
    .title{
      top: 20vw;
    }
  }
</style>
