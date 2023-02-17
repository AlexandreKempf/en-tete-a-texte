<script>
	import { pageTitle } from '../stores.js';

	$pageTitle = 'boutique';
</script>

<div class="pt-32">
	<div
		class="flex flex-col py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="w-full">
			<a href="https://enteteatexte.bandcamp.com/releases">
				<img class="object-cover w-full rounded-xl" src="album.jpg" alt="album-en-ligne" />
			</a>
		</div>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-4">
				<a href="https://enteteatexte.bandcamp.com/releases">L'album en ligne</a>
			</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Disponible sur <a href="https://enteteatexte.bandcamp.com/releases" class="text-sky-600">
					<b>bandcamp.com</b>
				</a>
			</p>
		</div>
	</div>

	<div class="m-auto text-center mt-20 mb-32">
		<h1 class="relative tracking-tight font-extrabold text-3xl">
			<p class="text-gray-900">Nous vendons aussi des fables et des livrets de paroles.</p>
			<a href="concerts" class="text-red-700">Venez les chercher en concerts !</a>
		</h1>
	</div>

	<div class="flex flex-wrap justify-center space-x-7 mt-20 mb-32 mx-auto">
		<img src="carpe-et-dilemme.jpg" class="w-96" />
		<img src="1984.jpg" class="w-96" />
		<img src="cocon-tige.jpg" class="w-96" />
	</div>
</div>
