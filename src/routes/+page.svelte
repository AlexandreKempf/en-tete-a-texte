<script>
	import { pageTitle } from './stores.js';

	$pageTitle = 'chanteurs';
</script>

<title>Gilles Le Cornec</title>

<div class="relative w-full xl:flex pt-16 xl:pt-0">
	<div class="w-full px-10 xl:inline-flex xl:w-1/2 xl:flex-col">
		<div class="max-w-xl py-10 m-auto">
			<h1 class="relative -left-1 tracking-tight font-extrabold text-6xl">
				<span class="text-sky-700">Gilles</span>
				<span class="text-gray-900">Le Cornec</span>
			</h1>

			<p class="text-xl text-gray-700 mt-5">
				est auteur, compositeur et interprète de ses chansons depuis quelques années. Épris de
				science et de littérature, il évolue dans le monde de la recherche en écologie marine
				pendant cinq années avant de s'en éloigner pour prendre le temps de voyager.
			</p>

			<p class="text-xl text-gray-700 mt-5">
				Océan indien, Asie du sud-est, Afrique de l'ouest influencent sa vision du monde et ses
				écrits, qu'il décide de mettre en musique. Après son premier duo "Barde à Vous", surtout
				actif à Belle-île-en-mer, il lance avec son frère Kergann le groupe "En tête à texte",
				projet de chansons à texte basé en Bretagne.
			</p>
		</div>
	</div>

	<div class="max-w-xl xl:w-1/2 xl:max-w-full mx-auto xl:mx-0">
		<img class="object-cover cropped-1 w-full" src="hero2.jpg" alt="gilles photo" />
	</div>
</div>

<div class="relative inline-flex flex-col-reverse xl:flex-row xl:flex w-full pt-10 xl:pt-0">
	<div class="max-w-xl xl:w-1/2 xl:max-w-full mx-auto xl:mx-0">
		<img class="object-cover cropped-2 w-full" src="hero3.jpg" alt="kergan photo" />
	</div>
	<div class="max-w-3xl xl:w-1/2 p-10 m-auto">
		<h1 class="relative -left-1 tracking-tight font-extrabold text-6xl">
			<span class="text-red-700">Kergann</span>
			<span class="text-gray-900">Le Cornec</span>
		</h1>
		<p class="text-xl text-gray-700 mt-5">
			est musicien, compositeur et interprète depuis sa plus tendre enfance. Très tôt il se met au
			piano et prête un grand intérêt à l'improvisation. Plus tard il testera tous les instruments
			qui lui tomberont entre les mains et la guitare restera l'un de ses instruments de
			prédilection.
		</p>
		<p class="text-xl text-gray-700 mt-5">
			Il est également passionné par les mathématiques et obtient son Doctorat en 2020. Après sa
			thèse, il décide finalement de s'écarter de la recherche pour se consacrer au groupe, lui
			permettant ainsi de découvrir le montage son et vidéo et d'étancher sa soif de musique !
		</p>
	</div>
</div>

<style>
	.cropped-1 {
		clip-path: polygon(30% 0, 0 100%, 100% 100%, 100% 0);
	}
	.cropped-2 {
		clip-path: polygon(0 0, 0 100%, 70% 100%, 100% 0);
	}
</style>
