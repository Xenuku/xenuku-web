<script>
	import { beforeUpdate, onMount } from 'svelte';
	import { writable } from 'svelte/store';

	export let name;
	export let url;
	export let small;
	const isLoaded = writable(false);
	beforeUpdate(() => {
		const smallPreload = new Image();
		smallPreload.src = small;
	});

	onMount(() => {
		const img = new Image();
		img.src = url;
		img.addEventListener('load', () => {
			isLoaded.set(true);
		});
	});
</script>

<div
	class="bg-gradient-to-r from-emerald-600 to-[#0275ce] min-h-[300px] max-w-[200px] min-w-[200px] overflow-hidden rounded-md">
	<div
		class="bg-center bg-cover min-h-[300px] max-h-[300px] min-w-[200px] blur-div {$isLoaded
			? 'loaded'
			: ''}"
		style="background-image:url({small})"
		init>
		{#if $isLoaded}
			<img
				loading="lazy"
				src={url}
				alt="Poster for {name}"
				class="min-h-[300px] max-h-[300px] p-1 hover:scale-105 duration-300 ease-in-out hover:cursor-pointer object-cover object-center" />
		{/if}
	</div>
	<p class="text-center text-white font-extrabold loaded">{name}</p>
</div>

<style>
	.blur-div > img {
		opacity: 0;
	}
	.blur-div.loaded > img {
		opacity: 1;
		transition: opacity 1200ms ease-out;
	}
</style>
