<script>
	import Project from '$lib/project.svelte';
	import ProjectAlt from '../../lib/project-alt.svelte';
</script>

<svelte:head>
	<title>Xenuku - Projects</title>
</svelte:head>

<h2 class="text-4xl text-center text-blue-400">Projects</h2>
<div class="mb-8 mt-4 flex flex-wrap gap-8 md:gap-28">
	<Project
		image="viccrash.png"
		name="VicCrash Viewer"
		url="https://github.com/Xenuku/VicCrash-Viewer">
		Something about this project
	</Project>
	<ProjectAlt
		image="sneakychats.png"
		name="Sneaky Chats"
		url="https://github.com/Xenuku/SneakyChats">
		Something about this project too
	</ProjectAlt>
</div>
