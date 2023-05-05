<script>
	import Card from '$lib/card.svelte';
	import Category from '$lib/category.svelte';
</script>

<svelte:head>
	<title>Xenuku - Personal</title>
</svelte:head>

<div>
	<h2 class="text-4xl text-center text-blue-400">Personal</h2>
	<Category categoryName="Currently Watching / Plan to Watch">
		<Card url="images/showswatching/onepiece.png" name="One Piece" />
		<Card url="images/showswatching/sevendeadlysins.jpg" name="The Seven Deadly Sins" />
		<Card url="images/showswatching/got.png" name="Game of Thrones" />
		<Card url="images/showswatching/startrek.png" name="All of Star Trek" />
	</Category>
	<Category categoryName="Currently Reading / Plan to Read">
		<Card url="images/books/dcc.jpg" name="Dungeon Crawler Carl #2" />
		<Card url="images/books/hwfwm.jpg" name="He Who Fights With Monsters" />
		<Card url="images/books/mistborn.jpg" name="Mistborn" />
		<Card url="images/books/leviathanwakes.jpg" name="Leviathan Wakes" />
		<Card url="images/books/theprimalhunter.jpg" name="The Primal Hunter #6" />
	</Category>
	<Category categoryName="Currently Playing / Plan to Play">
		<Card url="images/gamesplaying/osrs.jpg" name="OSRS" />
		<Card url="images/gamesplaying/runescape.jpg" name="Runescape" />
		<Card url="images/gamesplaying/hitman3.jpg" name="Hitman 3" />
		<Card url="images/gamesplaying/civ6.jpeg" name="Civilization VI" />
		<Card url="images/gamesplaying/tome.jpg" name="Tales of Maj'Eyal" />
	</Category>
	<Category categoryName="Loved Shows">
		<Card url="images/lovedshows/stargate.jpg" name="Stargate" />
		<Card url="images/lovedshows/dark.png" name="DARK" />
		<Card url="images/lovedshows/dragonball.png" name="Dragon Ball" />
		<Card url="images/lovedshows/invincible.png" name="Invincible" />
		<Card url="images/lovedshows/farscape.jpg" name="Farscape" />
		<Card url="images/lovedshows/theoffice.jpg" name="The Office" />
	</Category>
	<Category categoryName="Loved Movies">
		<Card url="images/lovedmovies/gunsakimbo.jpg" name="Guns Akimbo" />
		<Card url="images/lovedmovies/httyd.jpg" name="HTTYD" />
		<Card url="images/lovedmovies/klaus.jpg" name="Klaus" />
		<Card url="images/lovedmovies/scottpilgrim.jpg" name="Scott Pilgrim" />
		<Card url="images/lovedmovies/spaceballs.jpg" name="Spaceballs" />
		<Card url="images/lovedmovies/spiderverse.png" name="Into the Spider-Verse" />
	</Category>
</div>
