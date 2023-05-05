<script>
	import Card from '$lib/card.svelte';
	import Category from '$lib/category.svelte';
	import data from './data.json';
</script>

<svelte:head>
	<title>Xenuku - Personal</title>
</svelte:head>

<div>
	<h2 class="text-4xl text-center text-blue-400">A few things I enjoy</h2>
	<Category categoryName="Currently Watching / Plan to Watch">
		{#each data.watching as show}
			<Card url="images/watching/{show.image}" name={show.name} />
		{/each}
	</Category>
	<Category categoryName="Currently Reading / Plan to Read">
		{#each data.reading as book}
			<Card url="images/reading/{book.image}" name={book.name} />
		{/each}
	</Category>
	<Category categoryName="Currently Playing / Plan to Play">
		{#each data.playing as game}
			<Card url="images/playing/{game.image}" name={game.name} />
		{/each}
	</Category>
	<Category categoryName="Favourite Games">
		{#each data.favouriteGames as game}
			<Card url="images/lovedgames/{game.image}" name={game.name} />
		{/each}
	</Category>
	<Category categoryName="Favourite Shows">
		{#each data.favouriteShows as show}
			<Card url="images/lovedshows/{show.image}" name={show.name} />
		{/each}
	</Category>
	<Category categoryName="Favourite Movies">
		{#each data.favouriteMovies as movie}
			<Card url="images/lovedmovies/{movie.image}" name={movie.name} />
		{/each}
	</Category>
</div>
