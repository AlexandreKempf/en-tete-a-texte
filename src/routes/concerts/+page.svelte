<script>
	import { pageTitle } from '../stores.js';

	$pageTitle = 'concerts';
	// date start at 0 for months
	var concerts = [
		{
			date: new Date(2023, 3, 28, 19, 30),
			place: "Annivercirque, Quimperlé"
		},
		{
			date: new Date(2023, 4, 6, 16, 30),
			place: "Percu Corporelle (Gilles), Quimperlé"
		},
		{
			date: new Date(2023, 4, 6, 19, 30),
			place: "Brizeux, Quimperlé"
		},
		{
			date: new Date(2023, 4, 12, 22, 0),
			place: "Soirée à la grande salle Yhuel, Arzano"
		},
		{
			date: new Date(2023, 4, 13, 19, 0),
			place: "Bugul Noz Festival, Arzano"
		},
		{
			date: new Date(2023, 4, 14, 19, 0),
			place: "*Fête de la tonte, Bannalec"
		},
		{
			date: new Date(2023, 4, 19, 19, 0),
			place: "Mariage Privé, Trévignon"
		},
		{
			date: new Date(2023, 4, 26, 19, 0),
			place: "La Cave, Moëlan Sur Mer"
		},
		{
			date: new Date(2023, 4, 27, 19, 0),
			place: "Fête Privé, Bannalec"
		},
		{
			date: new Date(2023, 4, 28, 19, 0),
			place: "Festival de Conte, Plouray"
		},
		{
			date: new Date(2023, 5, 3, 19, 0),
			place: "La Chapelle, Locminé"
		},
		{
			date: new Date(2023, 5, 17, 19, 0),
			place: "*Arzano, Arzano"
		},
		{
			date: new Date(2023, 5, 18, 19, 0),
			place: "*Fête Pépinière, Bannalec"
		},
		{
			date: new Date(2023, 5, 24, 19, 0),
			place: "Fête de la musique, Riec Sur Bélon"
		},
		{
			date: new Date(2023, 6, 15, 19, 0),
			place: "L'Improbable Café, Plestin Les Grèves"
		},
		{
			date: new Date(2023, 6, 21, 20, 0),
			place: "Domaine de Beg Porz, Kerfany Les Pins"
		},
		{
			date: new Date(2023, 7, 4, 20, 0),
			place: "Domaine de Beg Porz, Kerfany Les Pins"
		},
		{
			date: new Date(2023, 7, 20, 19, 0),
			place: "Nuit des love shacks, Nizon"
		},
		{
			date: new Date(2023, 7, 25, 20, 0),
			place: "Domaine de Beg Porz, Kerfany Les Pins"
		},
	];

	var today = new Date();

	function dateToString(date) {
		const month = {
			0: 'Janv',
			1: 'Févr',
			2: 'Mars',
			3: 'Avril',
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
		<img class="object-cover w-full rounded-xl" src="Modif.jpg" alt="" />
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
						<div class="pl-2 text-xl w-36 flex-shrink-0 font-semibold tracking-wide uppercase">
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
