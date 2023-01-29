<script>
	import { YouTube } from 'sveltekit-embed';
	import { pageTitle } from '../stores.js';

	$pageTitle = 'chansons';
</script>

<div class="pt-32">
	<div
		class="flex flex-col py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="w-full">
			<YouTube youTubeId="Cz_uJi4p1Yw" />
		</div>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-2">Délivresse</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Cette chanson est une ôde à l'ivresse et a la délivrance. Duo de pochtrons. On pourrait en
				parler longtemps le but c'est juste d'avoir une introduction a la chanson ici.
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Papa Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Vidéo :</b> Le copain à Guillou
			</p>
		</div>
	</div>

	<div
		class="flex flex-col-reverse py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-2">Mélanie</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Hymne à la joie et à l'amour. La chanson s'inspire de la chanson paillarde Mélanie de
				Georges Brassens et raconte la vie de la nonne avant les ordres.
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Vidéo :</b> La mifa Le Cornec
			</p>
		</div>
		<div class="w-full">
			<YouTube youTubeId="9LLQcRczCeY" />
		</div>
	</div>

	<div
		class="flex flex-col py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="w-full">
			<YouTube youTubeId="fMz-s35aen8" />
		</div>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-2">Carpe Diem</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Cette chanson est une ôde à l'ivresse et a la délivrance. Duo de pochtrons. On pourrait en
				parler longtemps le but c'est juste d'avoir une introduction a la chanson ici.
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Papa Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Vidéo :</b> Le copain à Guillou
			</p>
		</div>
	</div>

	<div
		class="flex flex-col-reverse py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-2">Écrit après la visite d’un bagne</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Hymne à la joie et à l'amour. La chanson s'inspire de la chanson paillarde Mélanie de
				Georges Brassens et raconte la vie de la nonne avant les ordres.
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Vidéo :</b> La mifa Le Cornec
			</p>
		</div>
		<div class="w-full">
			<YouTube youTubeId="lpJZv09gOUM" />
		</div>
	</div>
	<div class="m-auto text-center mt-20 mb-32">
		<h1 class="relative tracking-tight font-extrabold text-3xl">
			<span class="text-gray-900">Découvrez nos autres chansons sur </span>
			<a href="https://www.youtube.com/@EnTeteATexte" class="text-red-700">YouTube</a>
		</h1>
	</div>
</div>
