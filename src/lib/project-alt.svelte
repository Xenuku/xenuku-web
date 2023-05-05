<script>
	export let name;
	export let image;
	export let url;
</script>

<div class="mt-8 mb-8">
	<h2 class="text-3xl text-center text-emerald-400">{name}</h2>
	<p class="text-center">
		<a class="text-blue-400 hover:text-emerald-400" href={url}>View on GitHub</a>
	</p>
	<div class="flex flex-wrap h-[400px]">
		<div class="bg-emerald-500 w-full md:w-1/2 p-5">
			<slot />
		</div>
		<div class="bg-blue-500 w-full md:w-1/2 p-5">
			<img src="images/projects/{image}" alt="Screenshot of {name} project" />
		</div>
	</div>
</div>
