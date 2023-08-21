<script>
  import data from '../../data/data.json';
  let crew = data.crew;

  let crewMember = crew[0];
</script>
<main class="bg-fixed bg-cover bg-[url(/assets/crew/background-crew-desktop.jpg) no-repeat] bg-[url(/assets/crew/background-crew-mobile.jpg) no-repeat] md:w-2/3 w-full md:flex-row flex-col md:mx-auto mt-[2rem]">
  <div>
    02 MEET YOUR CREW
  </div>
  <div class="md:mt-[2rem] flex md:flex-row flex-col gap-[2rem] justify-between">
    <div class="w-2/3">
      <div class="md:my-4 my-2 md:text-2xl text-xl">{crewMember.role}</div>
      <div class="md:my-4 my-2 md:text-4xl text-2xl xs:font-thin font-serif">{crewMember.name}</div>
      <div class="md:my-4 my-1 text-l xs:w-full">{crewMember.bio}</div>
      <div class="flex gap-[1rem]">
        {#each crew as mem}
        <button class="xs:text-4xl text-3xl" on:click={() => crewMember=mem}>&bull;</button>
        {/each}
      </div>
    </div>
    <div>
      <img src={crewMember.images.png} alt="img" />
    </div>
  </div>
</main>