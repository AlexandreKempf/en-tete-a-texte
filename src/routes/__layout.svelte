<script>
  import '../app.css';

  let current = 'index';
  const setCurrentIndex = () => (current = 'index');
  const setCurrentConcerts = () => (current = 'concerts');
  const setCurrentChansons = () => (current = 'chansons');
  const setCurrentParoles = () => (current = 'paroles');
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
        class="z-30 text-2xl font-bold {current == 'index'
          ? 'text-sky-600'
          : 'text-gray-900'} hover:text-red-700"
        on:click={setCurrentIndex}>Chanteurs</a
      >
      <a
        href="concerts"
        class="z-30 text-2xl font-bold {current == 'concerts'
          ? 'text-sky-600'
          : 'text-gray-900'} hover:text-red-700"
        on:click={setCurrentConcerts}>Concerts</a
      >
      <a
        href="chansons"
        class="z-30 text-2xl font-bold {current == 'chansons'
          ? 'text-sky-600'
          : 'text-gray-900'} hover:text-red-700"
        on:click={setCurrentChansons}>Chansons</a
      >
      <a
        href="#"
        class="z-30 grow text-2xl font-bold {current == 'paroles'
          ? 'text-sky-600'
          : 'text-gray-900'} hover:text-red-700"
        on:click={setCurrentParoles}>Paroles</a
      >
    </nav>
  </div>
</div>

<slot />
