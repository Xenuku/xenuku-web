<script>
	import Card from '$lib/card.svelte';
	import Category from '$lib/category.svelte';
	import data from './data.json';
</script>

<svelte:head>
	<title>Xenuku - Personal</title>
</svelte:head>

<div>
	<h2 class="text-4xl text-center text-[#F8F8F8]">
		Getting
		<span class="bg-gradient-to-r from-emerald-400 to-[#2a98ec] bg-clip-text text-transparent">
			Personal
		</span>
	</h2>
	<Category categoryName="Currently Watching / Planning to Watch">
		{#each data.watching as show}
			<Card
				small="images/watching/{show.small}"
				url="images/watching/{show.image}"
				name={show.name} />
		{/each}
	</Category>
	<Category categoryName="Currently Playing / Planning to Play">
		{#each data.playing as game}
			<Card
				small="images/playing/{game.small}"
				url="images/playing/{game.image}"
				name={game.name} />
		{/each}
	</Category>
	<Category categoryName="Currently Reading / Planning to Read">
		{#each data.reading as book}
			<Card
				small="images/reading/{book.small}"
				url="images/reading/{book.image}"
				name={book.name} />
		{/each}
	</Category>
	<Category categoryName="Favourite Games">
		{#each data.favouriteGames as game}
			<Card
				small="images/lovedgames/{game.small}"
				url="images/lovedgames/{game.image}"
				name={game.name} />
		{/each}
	</Category>
	<Category categoryName="Favourite Shows">
		{#each data.favouriteShows as show}
			<Card
				small="images/lovedshows/{show.small}"
				url="images/lovedshows/{show.image}"
				name={show.name} />
		{/each}
	</Category>
	<Category categoryName="Favourite Movies">
		{#each data.favouriteMovies as movie}
			<Card
				small="images/lovedmovies/{movie.small}"
				url="images/lovedmovies/{movie.image}"
				name={movie.name} />
		{/each}
	</Category>
</div>
