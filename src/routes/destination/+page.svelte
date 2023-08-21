<script>
  import data from '../../data/data.json';
  let destinations = data.destinations;

  let curDest = destinations[0];
</script>

<main class="bg-fixed bg-cover md:bg-[url(/assets/technology/background-destination-desktop.jpg)] bg-[url(/assets/technology/background-destination-mobile.jpg)]">
  <section class="md:mx-[10rem] mx-auto">
    <!-- <div class="flex md:flex-row flex-col md:mt-[10rem] mt-[2rem] md:justify-between text-2xl md:mr-[40rem]"> -->
    <div class="md:mt-[10rem] mt-[2rem] flex md:items-center flex-col md:flex-row">
      <div class="md:w-[60rem] mb-4">01 Pick your Destination</div>
      <div class="bg-[rgba(0,100,120,0.5)] md:p-[1rem] flex md:flex-row gap-2 md:gap-[2rem] p-2">
        {#each destinations as dest}
          <button on:click={() => {curDest=dest}} class="md:text-xl text-s">{dest.name}</button>
        {/each}
      </div>
    </div>
    <div class="flex md:flex-row md:gap-[4rem] gap-[2rem] flex-col">
      <div><img src={curDest.images.png} alt={curDest.name}></div>
      <div>
        <div class="mx:text-4xl text-2xl">{curDest.name}</div>
        <div>
          {curDest.description}
        </div>
        <hr class="my-4">
        <div class="flex gap-[8rem]">
          <div>
            <div class="uppercase font-thin font-[helvetica]">Avg. distance</div>
            <div class="uppercase text-2xl font-[Times]">{curDest.distance}</div>
          </div>
          <div>
            <div class="uppercase font-thin font-[helvetica]">travel time</div>
            <div class="uppercase text-2xl font-[Times]">{curDest.travel}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>