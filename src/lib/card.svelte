<script>
	export let name;
	export let url;
</script>

<div class="bg-gradient-to-r from-emerald-400 to-[#2a98ec] min-h-[300px] max-w-[200px]">
	<img src={url} alt="Poster for {name}" class="min-h-[300px] max-h-[300px] p-1" />
	<p class="text-center text-gray-800 text-sm">{name}</p>
</div>
