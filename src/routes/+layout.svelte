<script>
	import '../app.css';
	import { pageTitle } from './stores.js';
</script>

<title>En-Tête-en-Texte</title>
<div class="absolute flex w-full">
	<div class="inline-flex w-1/2 flex-col">
		<nav class="flex items-center gap-10">
			<button class="h-20 flex-none">
				<img alt="Menu" src="favicon.png" />
			</button>
			<a
				href="/"
				class="z-30 text-2xl font-bold {$pageTitle == 'index'
					? 'text-sky-600'
					: 'text-gray-900'} hover:text-red-700"
				on:click={() => ($pageTitle = 'index')}>Chanteurs</a
			>
			<a
				href="concerts"
				class="z-30 text-2xl font-bold {$pageTitle == 'concerts'
					? 'text-sky-600'
					: 'text-gray-900'} hover:text-red-700"
				on:click={() => ($pageTitle = 'concerts')}>Concerts</a
			>
			<a
				href="chansons"
				class="z-30 text-2xl font-bold {$pageTitle == 'chansons'
					? 'text-sky-600'
					: 'text-gray-900'} hover:text-red-700"
				on:click={() => ($pageTitle = 'chansons')}>Chansons</a
			>
			<a
				href="#"
				class="z-30 grow text-2xl font-bold {$pageTitle == 'paroles'
					? 'text-sky-600'
					: 'text-gray-900'} hover:text-red-700"
				on:click={() => ($pageTitle = 'paroles')}>Paroles</a
			>
		</nav>
	</div>
</div>

<slot />
