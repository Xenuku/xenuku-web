<script>
  import HobbySvg from './svgs/hobbySvg.svelte';
  import RecentSvg from './svgs/recentSvg.svelte';
  import SoloSvg from './svgs/soloSvg.svelte';
  import TeamSvg from './svgs/teamSvg.svelte';
  import UniSvg from './svgs/uniSvg.svelte';

  export let about;
  export let mainTechnology;
  export let technologies;
  export let type;
  export let projectType;

  let technologySymbols = {
    Python:
      'https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue',
    TypeScript:
      'https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white',
    PHP: 'https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white',
    Svelte: 'https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00'
  };
</script>

<div class="text-[#fbfbfb]">
  <div class="xl:flex">
    <div class="flex flex-wrap gap-1 mb-2">
      <img
        src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white"
        alt="VSCode Badge" />
      <img src={technologySymbols[mainTechnology]} alt="{mainTechnology} logo" /><br />
    </div>
    <div class="flex gap-1 flex-wrap">
      <span class="flex gap-1">
        {#if type == 'Team'}
          <TeamSvg />
        {:else}
          <SoloSvg />
        {/if}
        {type} project
      </span>
      <span class="flex gap-1">
        {#if projectType == 'University'}
          <UniSvg />
        {:else}
          <HobbySvg />
        {/if}
        {projectType}
      </span>
      <span class="flex gap-1">
        {#if mainTechnology == 'PHP'}
          <RecentSvg />
          Most Recent
        {/if}
      </span>
    </div>
  </div>

  <p class="my-2">
    {#each about as line}
      {line} <br /><br />
    {/each}
  </p>

  <div class="font-bold">Technologies</div>
  <ul class="indent-8">
    {#each technologies as tech}
      <li>{tech}</li>
    {/each}
  </ul>
</div>
