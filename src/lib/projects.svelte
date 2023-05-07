<script>
	import data from '$lib/project-data.json';
	import ProjectAbout from './project-about.svelte';
</script>

{#each data.projects as project}
	<div class="mt-8 mb-8">
		<h2 class="text-3xl text-center text-[#d4af37]">{project.name}</h2>
		<p class="text-center my-2">
			{#if project.url === 'PRIVATE'}
				<p class="text-emerald-400">Private Repository</p>
			{:else}
				<a class="text-blue-400 hover:text-emerald-400 inline-block" href={project.url}>
					<img
						src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"
						alt="GitHub Logo" />
				</a>
			{/if}
		</p>
		<div class="flex flex-wrap min-h-[30vh]">
			{#if project.alt}
				<div class="bg-[#4c5666] w-full md:w-1/2 p-5">
					<ProjectAbout
						about={project.about}
						mainTechnology={project.mainTechnology}
						technologies={project.technologies}
						type={project.type}
						projectType={project.project_type} />
				</div>
				<div class="bg-[#1a1a1a] w-full md:w-1/2 p-5">
					<img src="images/projects/{project.image}" alt="Screenshot of {project.name} project" />
				</div>
			{:else}
				<div class="bg-[#1a1a1a] w-full md:w-1/2 p-5">
					<img src="images/projects/{project.image}" alt="Screenshot of {project.name} project" />
				</div>
				<div class="bg-[#4c5666] w-full md:w-1/2 p-5">
					<ProjectAbout
						about={project.about}
						mainTechnology={project.mainTechnology}
						technologies={project.technologies}
						type={project.type}
						projectType={project.project_type} />
				</div>
			{/if}
		</div>
	</div>
{/each}
