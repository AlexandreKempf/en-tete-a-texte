<script>
	import '../app.css';
	import { pageTitle } from './stores.js';

	let screenSize;
	let navButtonClicked = false;

	function capitalizeFirstLetter(string) {
		return string.charAt(0).toUpperCase() + string.slice(1);
	}

	$: navButtonClicked = screenSize >= 1550;
	$: {
		$pageTitle;
		navButtonClicked = false;
	}
</script>

<title>En-Tête-en-Texte</title>
<div class="absolute flex w-full" bind:clientWidth={screenSize}>
	<div class="inline-flex w-1/2 flex-col">
		{#if screenSize >= 1550}
			<nav class="flex items-center gap-2 md:gap-10">
				<button class="h-20 flex-none">
					<img alt="Menu" src="favicon.jpg" class="h-20 lg:h-32" />
				</button>
				<a
					href="/"
					class="z-30 text-2xl pt-12 font-bold {$pageTitle == 'chanteurs'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Chanteurs</a
				>
				<a
					href="boutique"
					class="z-30 text-2xl pt-12 font-bold {$pageTitle == 'boutique'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Boutique</a
				>
				<a
					href="concerts"
					class="z-30 text-2xl pt-12 font-bold {$pageTitle == 'concerts'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Concerts</a
				>
				<a
					href="chansons"
					class="z-30 text-2xl pt-12 font-bold {$pageTitle == 'chansons'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Chansons</a
				>
				<a
					href="paroles"
					class="z-30 text-2xl pt-12 font-bold {$pageTitle == 'paroles'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Paroles</a
				>
				<a
					href="contact"
					class="z-30 grow text-2xl pt-12 font-bold {$pageTitle == 'contact'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Contact</a
				>
			</nav>
		{:else}
			<nav class="flex gap-2">
				<button
					class="h-20 flex-none z-10"
					on:click={() => {
						navButtonClicked = !navButtonClicked;
					}}
				>
					<img alt="Menu" src="favicon.jpg" class="h-20 lg:h-32" />
				</button>
				{#if navButtonClicked}
					<div
						class="flex flex-col bg-white z-10 mt-3 border-2 px-10 py-5 rounded-md border-color border-gray-900"
					>
						<a
							href="/"
							class="z-30 text-2xl font-bold {$pageTitle == 'chanteurs'
								? 'text-sky-600'
								: 'text-gray-900'} hover:text-red-700">Chanteurs</a
						>
						<a
							href="boutique"
							class="z-30 text-2xl font-bold {$pageTitle == 'boutique'
								? 'text-sky-600'
								: 'text-gray-900'} hover:text-red-700">Boutique</a
						>
						<a
							href="concerts"
							class="z-30 text-2xl font-bold {$pageTitle == 'concerts'
								? 'text-sky-600'
								: 'text-gray-900'} hover:text-red-700">Concerts</a
						>
						<a
							href="chansons"
							class="z-30 text-2xl font-bold {$pageTitle == 'chansons'
								? 'text-sky-600'
								: 'text-gray-900'} hover:text-red-700">Chansons</a
						>
						<a
							href="paroles"
							class="z-30 text-2xl font-bold {$pageTitle == 'paroles'
								? 'text-sky-600'
								: 'text-gray-900'} hover:text-red-700">Paroles</a
						>
						<a
							href="contact"
							class="z-30 grow text-2xl font-bold {$pageTitle == 'contact'
								? 'text-sky-600'
								: 'text-gray-900'} hover:text-red-700">Contact</a
						>
					</div>
				{:else}
					<p class="z-30 grow pt-7 lg:pt-12 text-2xl font-bold text-gray-900">
						{capitalizeFirstLetter($pageTitle)}
					</p>
				{/if}
			</nav>
		{/if}
	</div>
</div>

<slot />
