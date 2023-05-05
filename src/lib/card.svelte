<script>
	export let name;
	export let url;
</script>

<div
	class="bg-gradient-to-r from-emerald-600 to-[#0275ce] min-h-[300px] max-w-[200px] overflow-hidden">
	<img
		src={url}
		alt="Poster for {name}"
		class="min-h-[300px] max-h-[300px] p-1 hover:scale-105 duration-300 ease-in-out hover:cursor-pointer" />
	<p class="text-center text-white text-xl">{name}</p>
</div>
