<script>
  import data from '../../data/data.json';
  let techs = data.technology;

  let curTech = techs[0];
</script>

<main class="bg-fixed bg-cover m-auto md:bg-[url(/assets/technology/background-technology-desktop.jpg)] bg-[url(/assets/technology/background-technology-mobile.jpg)]">
  <section class="md:mx-[10rem]">
    <div class="md:text-3xl text-l md:mt-[4rem] mt-[4rem] uppercase">03 TECHNOLOGY</div>
    <div class="flex md:flex-row flex-col md:mx-[4rem] mx-2 md:gap-[3rem] gap-[2rem]">
      <div class="col-span-1 flex md:flex-col flex-row gap-4">
        {#each techs as tech,idx }
          <button on:click={() => {curTech=tech}} class="border rounded-full w-12 h-12">{idx+1}</button>
        {/each}
      </div>
      <div class="md:w-3/4 w-full flex flex-col md:gap-[2rem] gap-[1rem]">
        <div>The technology...</div>
        <div class="text-3xl">{curTech.name}</div>
        <div>{curTech.description}</div>
      </div>
      <div class="w-auto">
        <div class="md:visible invisible"><img src={curTech.images.landscape} alt=""></div>
        <div class="md:invisible visible"><img src={curTech.images.portrait} alt=""></div>
      </div>
      <!-- <div>
        {JSON.stringify(curTech)}
      </div> -->
    </div>
  </section>
</main>