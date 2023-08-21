<style>
  
</style>

<!-- <main style="background-image: url(/assets/technology/background-technology-desktop.jpg) no-repeat;background-size:cover;"> -->
<main class="bg-fixed bg-cover h-[100vh] bg-black bg-no-repeat bg-[url(/assets/home/background-home-desktop.jpg)] text-white p-[2rem]">
  <nav class="flex justify-between">
    <img id="desktop-logo" src="/assets/shared/logo.svg" class="flex md:visible md:justify-start" alt="logo" />
    <img id="mobile-logo" class="xs:visible md:hidden" src="/assets/shared/icon-hamburger.svg" alt="logo" />
    <div class="flex items-center md:px-[2rem] md:gap-[2rem] gap-[1rem] md:bg-[rgba(10,100,120,0.5)]">
      <a href="/">00 Home</a>
      <a href="/destination">01 Destination</a>
      <a href="/crew">02 Crew</a>
      <a href="/technology">03 Technology</a>
    </div>
  </nav>
  <div>
    <slot />
  </div>
</main>