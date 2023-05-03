<script>
	import '../app.css';
	import NavLink from '$lib/nav-link.svelte';
	import { slide } from 'svelte/transition';
	let open = false;
</script>

<nav class="w-full px-8 py-4 bg-slate-500 text-white">
	<div class="hidden sm:flex justify-between">
		<a href="/" class="text-xl">Xenuku</a>
		<div>
			<a class="hover:text-blue-400" href="/">Home</a>
			<a class="hover:text-blue-400 pl-2" href="/blog">Blog</a>
			<a class="hover:text-blue-400 pl-2" href="/personal">Personal</a>
		</div>
	</div>
	<div class="flex justify-between sm:hidden">
		<a href="/" class="text-xl p-2">Xenuku</a>
		<!-- Hamburger -->
		<div class="-mr-2 flex items-center sm:hidden">
			<button
				on:click={() => (open ? (open = false) : (open = true))}
				class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 dark:text-gray-500 hover:text-gray-500 dark:hover:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-900 focus:outline-none focus:bg-gray-100 dark:focus:bg-gray-900 focus:text-gray-500 dark:focus:text-gray-400 transition duration-150 ease-in-out"
			>
				<svg class="h-6 w-6" stroke="#C4C4C4" fill="none" viewBox="0 0 24 24">
					<path
						class={open ? 'hidden' : 'inline-flex'}
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M4 6h16M4 12h16M4 18h16"
					/>
					<path
						class={open ? 'inline-flex' : 'hidden'}
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M6 18L18 6M6 6l12 12"
					/>
				</svg>
			</button>
		</div>
	</div>
	{#if open}
		<div class="{open ? 'block' : 'hidden'} sm:hidden" transition:slide>
			<NavLink route="/" linkText="Home" />
			<NavLink route="/personal" linkText="Personal" />
			<NavLink route="/blog" linkText="Blog" />
		</div>
	{/if}
</nav>
<div class="px-8 pt-2 bg-gray-800 min-h-screen">
	<slot />
</div>
