<script>
	import { pageTitle } from '../stores.js';
	import { concerts, dateToString } from '../concerts.js';

	$pageTitle = 'historique';

	var today = new Date();

	const scrollToBottom = (node) => {
		const scroll = () =>
			node.scroll({
				left: node.scrollWidth,
				behavior: 'instant' // or 'smooth'
			});
		scroll();

		return { update: scroll };
	};
</script>

<div
	use:scrollToBottom={concerts}
	class="flex flex-col-reverse lg:flex-row w-full pt-32 overflow-x-scroll"
>
	<ol class="lg:w-1/2 pl-10 lg:pl-0 flex">
		{#each concerts as concert}
			<li class="relative pb-10">
				<div
					class="-ml-px absolute mt-0.5 top-4 left-4 w-full h-0.5 bg-blue-600"
					aria-hidden="true"
				/>
				{#if concert.date < today}
					<div class="flex-col items-start group mx-3">
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
						<div class="font-Inter relative top-1">
							<div class="text-xl w-36 flex-shrink-0 font-semibold tracking-wide uppercase">
								{dateToString(concert.date)}
							</div>
							<div
								class="text-large -mt-1 mb-2 flex-shrink-0 font-semibold tracking-wide uppercase"
							>
								{concert.date.getFullYear().toString()}
							</div>
							<div class="min-w-0 flex flex-col">
								<div class="text-sm tracking-wide">
									{concert.place}
								</div>
							</div>
						</div>
					</div>
				{/if}
			</li>
		{/each}
	</ol>
</div>
