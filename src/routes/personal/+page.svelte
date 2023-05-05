<script>
	import Card from '$lib/card.svelte';
	import Category from '$lib/category.svelte';
	let reading = 'images/books';
	let playing = 'images/gamesplaying';
	let watching = 'images/showswatching';
	let lovedShows = 'images/lovedshows';
	let lovedGames = 'images/lovedgames';
	let lovedMovies = 'images/lovedmovies';
</script>

<svelte:head>
	<title>Xenuku - Personal</title>
</svelte:head>

<div>
	<h2 class="text-4xl text-center text-blue-400">A few things I enjoy</h2>
	<Category categoryName="Currently Watching / Plan to Watch">
		<Card url="{watching}/onepiece.png" name="One Piece" />
		<Card url="{watching}/sevendeadlysins.jpg" name="The Seven Deadly Sins" />
		<Card url="{watching}/got.png" name="Game of Thrones" />
		<Card url="{watching}/startrek.png" name="All of Star Trek" />
	</Category>
	<Category categoryName="Currently Reading / Plan to Read">
		<Card url="{reading}/dcc.jpg" name="Dungeon Crawler Carl #2" />
		<Card url="{reading}/hwfwm.jpg" name="He Who Fights With Monsters" />
		<Card url="{reading}/mistborn.jpg" name="Mistborn" />
		<Card url="{reading}/leviathanwakes.jpg" name="Leviathan Wakes" />
		<Card url="{reading}/theprimalhunter.jpg" name="The Primal Hunter #6" />
	</Category>
	<Category categoryName="Currently Playing / Plan to Play">
		<Card url="{playing}/osrs.jpg" name="OSRS" />
		<Card url="{playing}/runescape.jpg" name="Runescape" />
		<Card url="{playing}/hitman3.jpg" name="Hitman 3" />
		<Card url="{playing}/civ6.jpeg" name="Civilization VI" />
		<Card url="{playing}/tome.jpg" name="Tales of Maj'Eyal" />
	</Category>
	<Category categoryName="Favourite Games">
		<Card url="{lovedGames}/drg.jpg" name="Deep Rock Galactic" />
		<Card url="{lovedGames}/animalcrossing.jpg" name="Animal Crossing" />
		<Card url="{lovedGames}/banjokazooie.jpg" name="Banjo Kazooie" />
		<Card url="{lovedGames}/mhw.jpg" name="Monster Hunter: World" />
		<Card url="{lovedGames}/p5r.png" name="Persona 5 Royal" />
		<Card url="{lovedGames}/supraland.jpg" name="Supraland" />
	</Category>
	<Category categoryName="Favourite Shows">
		<Card url="{lovedShows}/stargate.jpg" name="Stargate" />
		<Card url="{lovedShows}/dark.png" name="DARK" />
		<Card url="{lovedShows}/dragonball.png" name="Dragon Ball" />
		<Card url="{lovedShows}/invincible.png" name="Invincible" />
		<Card url="{lovedShows}/farscape.jpg" name="Farscape" />
		<Card url="{lovedShows}/theoffice.jpg" name="The Office" />
	</Category>
	<Category categoryName="Favourite Movies">
		<Card url="{lovedMovies}/gunsakimbo.jpg" name="Guns Akimbo" />
		<Card url="{lovedMovies}/httyd.jpg" name="HTTYD" />
		<Card url="{lovedMovies}/klaus.jpg" name="Klaus" />
		<Card url="{lovedMovies}/scottpilgrim.jpg" name="Scott Pilgrim" />
		<Card url="{lovedMovies}/spaceballs.jpg" name="Spaceballs" />
		<Card url="{lovedMovies}/spiderverse.png" name="Into the Spider-Verse" />
	</Category>
</div>
