<script>
	import data from '$lib/project-data.json';
	import { onMount } from 'svelte';
	import ProjectAbout from './project-about.svelte';
	let wrapper;
	let imgLoaded = false;

	onMount(() => {
		let divBlurs = wrapper.querySelectorAll('.blur-div');
		divBlurs.forEach((div) => {
			let img = div.querySelector('img');
			function loaded() {
				imgLoaded = true;
			}
			if (img.complete) {
				loaded();
			} else {
				img.addEventListener('load', loaded());
			}
		});
	});
</script>

{#each data.projects as project}
	<div class="mt-8 mb-8" bind:this={wrapper}>
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
				<div class="flex-wrap-reverse flex lg:flex-wrap">
					<div class="bg-[#4c5666] w-full lg:w-1/2 p-5">
						<ProjectAbout
							about={project.about}
							mainTechnology={project.mainTechnology}
							technologies={project.technologies}
							type={project.type}
							projectType={project.project_type} />
					</div>
					<div class="bg-[#1a1a1a] w-full lg:w-1/2 p-5">
						<div
							class="bg-cover bg-center min-w-full min-h-full blur-div"
							class:loaded={imgLoaded}
							style="background-image:url('images/projects/{project.small}')">
							<img
								loading="lazy"
								src="images/projects/{project.image}"
								alt="Screenshot of {project.name} project" />
						</div>
					</div>
				</div>
			{:else}
				<div class="bg-[#1a1a1a] w-full lg:w-1/2 p-5">
					<div
						class="bg-cover bg-center min-w-full min-h-full blur-div"
						class:loaded={imgLoaded}
						style="background-image:url('images/projects/{project.small}')">
						<img
							src="images/projects/{project.image}"
							alt="Screenshot of {project.name} project"
							loading="lazy" />
					</div>
				</div>
				<div class="bg-[#4c5666] w-full lg:w-1/2 p-5">
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

<style>
	.blur-div > img {
		opacity: 0;
	}
	.blur-div.loaded > img {
		opacity: 1;
		transition: opacity 1200ms ease-out;
	}
</style>
