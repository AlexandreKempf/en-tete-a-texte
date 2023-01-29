<script>
	import { pageTitle } from '../stores.js';

	$pageTitle = 'concerts';
	// date start at 0 for months
	var concerts = [
		{ date: new Date(2022, 5, 10, 20, 0), place: 'Ty Pouce, Quimperlé' },
		{
			date: new Date(2022, 5, 19, 16, 30),
			place: 'La bascule, ArGoat'
		},
		{
			date: new Date(2022, 5, 21, 21, 0),
			place: 'Fêtes de la musique, Runan'
		},
		{
			date: new Date(2022, 5, 24, 20, 30),
			place: 'bar de La Mi-Temps bouille, Saint Brieuc'
		},
		{
			date: new Date(2022, 6, 8, 19, 0),
			place: 'Kurnig Kafé, Guissény'
		},
		{
			date: new Date(2022, 6, 18, 18, 30),
			place: 'La Godaille, Belle-Île-en-Mer'
		},
		{
			date: new Date(2022, 6, 19, 21, 0),
			place: 'Matelo, Belle-Île-en-Mer'
		},
		{
			date: new Date(2022, 6, 20, 19, 0),
			place: 'Mabalulu, Locmaria'
		},
		{
			date: new Date(2022, 6, 22, 19, 30),
			place: "Camping de l'océan, Belle-Île-en-Mer"
		},
		{
			date: new Date(2022, 6, 24, 21, 30),
			place: 'Nul Bar After, Sauzon'
		},
		{
			date: new Date(2022, 6, 27, 19, 30),
			place: 'Domaine Maritime de Beg Porz, Moëlan-sur-Mer'
		}
	];

	var today = new Date();

	function dateToString(date) {
		const month = {
			0: 'Janv',
			1: 'Févr',
			2: 'Mars',
			3: 'Avri',
			4: 'Mai',
			5: 'Juin',
			6: 'Juil',
			7: 'Août',
			8: 'Sept',
			9: 'Oct',
			10: 'Nov',
			11: 'Déc'
		}[date.getMonth()];
		return date.getDate().toString() + ' ' + month.toString();
	}

	function timeToString(date) {
		const day = {
			0: 'Dimanche',
			1: 'Lundi',
			2: 'Mardi',
			3: 'Mercredi',
			4: 'Jeudi',
			5: 'Vendredi',
			6: 'Samedi'
		}[date.getDay()];

		const hour = date.getHours();
		const minutes =
			date.getMinutes() < 10 ? '0' + date.getMinutes().toString() : date.getMinutes().toString();
		return day.toString() + ' à ' + hour.toString() + ':' + minutes;
	}
</script>

<div class="flex flex-col-reverse lg:flex-row w-full pt-32">
	<div class="lg:w-1/3 mx-10 lg:mx-auto pt-10 lg:pt-0">
		<img class="object-cover w-full rounded-xl" src="hero4.jpg" alt="" />
	</div>
	<ol class="lg:w-1/2 pl-10 lg:pl-0">
		{#each concerts as concert}
			<li class="relative pb-10">
				<div
					class="-ml-px absolute mt-0.5 top-4 left-4 w-0.5 h-full bg-sky-600"
					aria-hidden="true"
				/>
				<div class="flex items-start group">
					{#if concert.date < today}
						<span class="h-9 flex items-center">
							<span
								class="z-10 w-8 h-8 flex items-center justify-center bg-sky-600 rounded-full group-hover:bg-sky-600"
							>
								<svg
									class="w-5 h-5 text-white"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
										clip-rule="evenodd"
									/>
								</svg>
							</span>
						</span>
					{:else if (concert.date - today) / (1000 * 60 * 60 * 24) < 7}
						<span class="h-9 flex items-center" aria-hidden="true">
							<span
								class="relative z-10 w-8 h-8 flex items-center justify-center bg-white border-2 border-sky-600 rounded-full"
							>
								<span class="h-2.5 w-2.5 bg-sky-600 rounded-full" />
							</span>
						</span>
					{:else}
						<span class="h-9 flex items-center" aria-hidden="true">
							<span
								class="relative z-10 w-8 h-8 flex items-center justify-center bg-white border-2 border-gray-300 rounded-full group-hover:border-gray-400"
							>
								<span class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" />
							</span>
						</span>
					{/if}
					<div class="font-Inter relative flex top-1">
						<div class="pl-2 text-xl w-24 flex-shrink-0 font-semibold tracking-wide uppercase">
							{dateToString(concert.date)}
						</div>
						<div class="ml-4 min-w-0 flex flex-col">
							<div class="text-sm font-semibold tracking-wide uppercase">
								{concert.place}
							</div>
							<div class="text-sm text-gray-500">
								{timeToString(concert.date)}
							</div>
						</div>
					</div>
				</div>
			</li>
		{/each}
	</ol>
</div>
