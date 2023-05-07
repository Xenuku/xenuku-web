<script>
	import Project from '$lib/project.svelte';
</script>

<svelte:head>
	<title>Xenuku - Projects</title>
</svelte:head>

<h2 class="text-4xl text-center text-blue-400">Projects</h2>
<div class="mb-8 mt-4 flex flex-wrap justify-between">
	<Project
		image="viccrash.png"
		name="VicCrash Viewer"
		url="https://github.com/Xenuku/VicCrash-Viewer">
		<p>
			Team based project with the goal of creating an interactive user interface to visualise and
			search a large excel based datafile. Includes a user manual and useable on Windows and Linux.
		</p>
		<span class="font-bold">Technologies used:</span>
		<ul class="indent-8">
			<li>Python</li>
			<li>PyQt5</li>
			<li>Matplotlib</li>
			<li>SQL, SQLite</li>
			<li>Git and GitHub</li>
		</ul>
	</Project>
	<Project
		image="sneakychats.png"
		alt="true"
		name="Sneaky Chats"
		url="https://github.com/Xenuku/SneakyChats">
		<p>
			Solo project with the goal of creating a real time, multiple room chat application with
			varying levels of user permissions. Images and chat history are supported per invidual room.
		</p>
		<span class="font-bold">Technologies used:</span>
		<ul class="indent-8">
			<li>JavaScript/TypeScript/Angular</li>
			<li>Node.js</li>
			<li>Express.js</li>
			<li>MongoDB</li>
			<li>Sockets.io</li>
			<li>Git and GitHub</li>
		</ul>
	</Project>
	<Project image="viccrash.png" name="HabITech Builder" url="PRIVATE">
		<p>
			Team based project with the goal of creating an interactive user interface to visualise and
			search a large excel based datafile. Includes a user manual and useable on Windows and Linux.
		</p>
		<span class="font-bold">Technologies used:</span>
		<ul class="indent-8">
			<li>Python</li>
			<li>PyQt5</li>
			<li>Matplotlib</li>
			<li>SQL, SQLite</li>
			<li>Git and GitHub</li>
		</ul>
	</Project>
</div>
