<script>
	export let route;
	export let linkText;
</script>

<a href={route}>
	<p class="hover:text-blue-400 mt-3 p-2 hover:bg-slate-900 w-full">{linkText}</p>
</a>
