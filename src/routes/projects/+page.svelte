<script>
	import Projects from '$lib/projects.svelte';
</script>

<svelte:head>
	<title>Xenuku - Projects</title>
</svelte:head>

<h2 class="text-4xl text-center text-[#F8F8F8]">
	Some of my
	<span class="bg-gradient-to-r from-emerald-400 to-[#2a98ec] bg-clip-text text-transparent">
		Projects
	</span>
</h2>
<div class="mb-8 mt-4 flex flex-wrap justify-between">
	<Projects />
</div>
