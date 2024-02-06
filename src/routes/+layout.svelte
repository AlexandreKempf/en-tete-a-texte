<script>
	// analytics
	import { dev } from '$app/environment';
	import { inject } from '@vercel/analytics';
	inject({ mode: dev ? 'development' : 'production' });

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
				<a href="/" class="h-20 lg:h-32 flex-none z-30">
					<img alt="Menu" src="favicon.jpg" class="h-20 lg:h-32 flex-none" />
				</a>
				<a
					href="chanteurs"
					class="z-30 text-2xl pt-2 font-bold {$pageTitle == 'chanteurs'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Chanteurs</a
				>
				<a
					href="boutique"
					class="z-30 text-2xl pt-2 font-bold {$pageTitle == 'boutique'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Boutique</a
				>
				<a
					href="concerts"
					class="z-30 text-2xl pt-2 font-bold {$pageTitle == 'concerts'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Concerts</a
				>
				<a
					href="historique"
					class="z-30 text-2xl pt-2 font-bold {$pageTitle == 'historique'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Historique</a
				>
				<a
					href="chansons"
					class="z-30 text-2xl pt-2 font-bold {$pageTitle == 'chansons'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Chansons</a
				>
				<a
					href="paroles"
					class="z-30 text-2xl pt-2 font-bold {$pageTitle == 'paroles'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Paroles</a
				>
				<a
					href="contact"
					class="z-30 grow text-2xl pt-2 font-bold {$pageTitle == 'contact'
						? 'text-sky-600'
						: 'text-gray-900'} hover:text-red-700">Contact</a
				>
			</nav>
		{:else}
			<a href="/" class="absolute left-0 top-0 h-20 w-20 lg:h-32 lg:w-32 z-30">
				<img alt="icon" src="favicon.jpg" class="absolute left-0 top-0 h-20 w-20 lg:h-32 lg:w-32" />
			</a>
			{#if navButtonClicked}
				<div
					class="absolute right-16 top-10 lg:right-28 lg:top-16 flex flex-col bg-white z-10 border-2 px-10 py-5 rounded-md border-color border-gray-900"
				>
					<a
						href="chanteurs"
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
						href="historique"
						class="z-30 text-2xl font-bold {$pageTitle == 'historiques'
							? 'text-sky-600'
							: 'text-gray-900'} hover:text-red-700">Historique</a
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
			{/if}
			<p class="absolute left-20 top-6 lg:left-32 lg:top-12 text-2xl font-bold text-gray-900">
				{capitalizeFirstLetter($pageTitle)}
			</p>
			<button
				class="absolute top-1 right-0 z-10"
				on:click={() => {
					navButtonClicked = !navButtonClicked;
				}}
				><img src="menu.svg" alt="menu" class="h-32 w-32 lg:h-48 lg:w-48" />
			</button>
		{/if}
	</div>
</div>

<slot />
