<script>
  import { Router, Link } from "svelte-routing";
</script>

<footer class='bg-thirdly-900'>

<div class='block text-center sm:flex sm:justify-between sm:mx-36'>
  <img src='/logo.png' alt='Futarigoto logo'class='w-24 h-full mx-auto my-0 pt-12 pb-10 sm:mx-0 sm:pb-36 sm:w-36'/>

  <div class='flex justify-between px-10 sm:block sm:pt-8'>
    <Router>
      <span class='linkHover'><Link class='block sm:text-left' to="/">Home</Link></span>
      <span class='linkHover'><Link class='block sm:text-left' to="about">フタリゴトとは？</Link></span>
      <span class='linkHover'><Link class='block sm:text-left' to="episodes">エピソード</Link></span>
    </Router>
  </div>

  <div class='flex justify-between px-36 py-10 sm:py-16 sm:px-16 sm:justify-left sm:w-64 sm:mx-10'>
    <a href="https://www.youtube.com/channel/UCchbTyG85v9G_9QtOfNSSaw" target="_blank" rel="noopener noreferrer">
      <div class='youtubeLink' />
    </a>
    <a href="https://m.facebook.com/pg/%E4%BB%99%E5%8F%B0%E9%AB%98%E7%AD%89%E5%B0%82%E9%96%80%E5%AD%A6%E6%A0%A1%E3%83%AD%E3%83%9C%E3%83%86%E3%82%A3%E3%82%AF%E3%82%B9%E3%82%B3%E3%83%BC%E3%82%B9-1903009249795439/posts/?ref=page_internal&msite_tab_async=1" target="_blank" rel="noopener noreferrer">
      <div class='facebookLink' />
    </a>
  </div>
</div>

<div class="bar"/>
<p class='copyright'>2022 Robotics Course｜National Institute of Technology, Sendai College</p>
</footer>

<style>
  .linkHover {
    color: #FFFFFF;
    font-weight: bold;
    font-size: 0.875rem;
    padding: 0px 10px;
  }
  .copyright {
    color: #FFFFFF;
    font-size: 0.5rem;
    padding: 25px 0px;
  }
  .bar {
      margin: 0 auto;
      width: 90%;
      border-style: solid;
      border-color: #FFFFFF;
      border-width: 0.5px;
      height: 0;
  }
  .linkHover:hover {
        color: #FFDA77;
        transition: color 0.2s linear;
    }
  .youtubeLink {
    width: 40px;
    height: 40px;
    background:url('/youtube_social_circle_red.png');
    background-size: contain;
  }
  .youtubeLink:hover {
    background:url('/youtube_social_circle_white.png');
    background-size: contain;
  }
  .facebookLink {
    width: 40px;
    height: 40px;
    background:url('/f_logo_RGB-Blue_114.png');
    background-size: contain;
  }
  .facebookLink:hover {
    background:url('/f_logo_RGB-White_114.png');
    background-size: contain;
  }



</style>
