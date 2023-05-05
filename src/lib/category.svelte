<script>
	export let categoryName;
</script>

<div class="mt-12">
	<h2 class="text-4xl text-center md:text-left text-white mb-4">{categoryName}</h2>
	<div class="flex flex-wrap gap-8 mb-4 justify-center md:justify-normal">
		<slot />
	</div>
</div>
