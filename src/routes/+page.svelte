<script>
	import { pageTitle } from './stores.js';
	import { fly } from 'svelte/transition';

	$pageTitle = 'accueil';
</script>

<div class="pt-32">
	<div class="w-10/12 xl:w-6/12 mt-10 mx-10">
		<h1 class="my-14 font-bold text-5xl">En tête à texte</h1>
		<p class="mx-5 lg:mx-0 my-5 font-light text-xl">
			En tête à texte est un duo de chanson française, créé début 2021 par deux frères adeptes de
			poésie et de musique.
		</p>
		<p class="mx-5 lg:mx-0 my-5 font-light text-xl">
			Le but du projet ? Faire passer des messages à travers le rire, la colère, la tristesse tout
			en partageant le goût du texte au public. Selon eux, l'art est une approche sensible qui, en
			faisant rêver, doit questionner, contester et idéalement fédérer. De facto, de grands concepts
			tels l'amour, le temps, l'absurdité humaine sont des thématiques récurrentes au sein de leurs
			compositions et de leurs influences (Brassens, Rostand, La Fontaine).
		</p>
		<p class="mx-5 lg:mx-0 my-5 font-light text-xl">
			La poésie se suffisant souvent à elle-même, les moyens de l'habiller sont nombreux, et
			l'éclectisme est de mise. Une vingtaine de compositions pour quatre-vingt-dix minutes de
			spectacle, au cours duquel des fables théâtralisées se glissent, les instruments s'échangent
			et les rythmes et harmonies surprennent. Tous deux pianistes, guitaristes et chanteurs, ils
			ont su créer un univers musical riche (intervention de beatbox, guimbarde, mélodica) aux
			influences manouches et folk.
		</p>
		<p class="mx-5 lg:mx-0 my-5 font-light text-xl">
			L'année 2022 a été clef pour le groupe, avec la création de leur premier album, de quatre
			livrets illustrés et du spectacle qui a tourné en Bretagne, dans les bars (notamment du
			finistère sud et de belle-île-en-mer), les festivals (Plein' R, les Tribus en Folies, fête de
			la musique) et dans la rue.
		</p>
		<p class="mx-5 lg:mx-0 my-5 font-light text-xl">
			À présent, le groupe se tourne également vers des lieux plus intimistes (café-librairie,
			médiathèque, concert chez l'habitant, festival de conte et de chanson française) à la
			recherche d'une écoute attentionnée.
		</p>
		<a href="concerts">
			<p class="mx-5 lg:mx-0 mt-5 text-2xl font-bold">Venez les découvrir !</p>
		</a>
	</div>
	<img
		class="xl:fixed xl:right-0 xl:bottom-0 w-full xl:w-5/12 mx-auto object-contain"
		src="test_acceuil.jpg"
		alt="the duo on stage"
	/>
</div>
