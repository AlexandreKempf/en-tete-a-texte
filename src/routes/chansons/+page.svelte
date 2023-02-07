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
				Cette chanson est une ôde à l'ivresse et a la délivrance. Chanson de marin écrite par le padre ! 
				En direct du Marimba Tyfolie Club.
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Pierre Marcel Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Kergann, Gilles et Stan Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Vidéo :</b> Aerieal Takof Productions
			</p>
		</div>
	</div>

	<div
		class="flex flex-col-reverse py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-2">Mélanie</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Hymne à la joie et à l'amour. La chanson et un hommage à la chanson paillarde "Mélanie" de
				Georges Brassens et raconte la vie de la nonne avant les ordres.
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
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
			<h1 class="text-7xl font-extralight tracking-wide py-2">Carpe et Dilemme</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Première fable illustrée. Une carpe aspirant au chant et à la musique !
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
			</p>
			<p class="text-sm text-gray-700">
				<b>Images :</b> Nolwenn Richard
			</p>
		</div>
	</div>

	<div
		class="flex flex-col-reverse py-10 xl:py-20 lg:flex-row w-2/3 lg:w-4/5 xl:w-2/3 mx-auto items-center gap-2 lg:gap-20"
	>
		<div class="lg:w-1/2">
			<h1 class="text-7xl font-extralight tracking-wide py-2">Écrit après la visite d’un bagne</h1>
			<p class="text-sm text-gray-700 italic py-1">
				Mise en musique d'un texte de Victor Hugo ! Live au Violon Vert !
			</p>
			<p class="text-sm text-gray-700">
				<b>Paroles :</b> Victor Hugo
			</p>
			<p class="text-sm text-gray-700">
				<b>Musique :</b> Gilles Le Cornec
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
