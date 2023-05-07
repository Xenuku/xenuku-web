<script>
	export let name;
	export let image;
	export let url;
	export let alt = false;
</script>

<div class="mt-8 mb-8">
	<h2 class="text-3xl text-center text-emerald-400">{name}</h2>
	<p class="text-center">
		{#if url === 'PRIVATE'}
			<p class="text-emerald-400">Private Repository</p>
		{:else}
			<a class="text-blue-400 hover:text-emerald-400" href={url}>View on GitHub</a>
		{/if}
	</p>
	<div class="flex flex-wrap min-h-[30vh]">
		{#if alt}
			<div class="bg-emerald-500 w-full md:w-1/2 p-5">
				<slot />
			</div>
			<div class="bg-blue-500 w-full md:w-1/2 p-5">
				<img src="images/projects/{image}" alt="Screenshot of {name} project" />
			</div>
		{:else}
			<div class="bg-blue-500 w-full md:w-1/2 p-5">
				<img src="images/projects/{image}" alt="Screenshot of {name} project" />
			</div>
			<div class="bg-emerald-500 w-full md:w-1/2 p-5">
				<slot />
			</div>
		{/if}
	</div>
</div>
