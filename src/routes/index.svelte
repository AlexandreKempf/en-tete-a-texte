<script>
    var menuIsHidden = false;

    function hideMenu() {
        menuIsHidden = false;
    }

    function displayMenu() {
        menuIsHidden = true;
    }
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
                Originaire des Côtes d’Armor, où il a été formé musicalement,
                Gilles Le Cornec est auteur, compositeur et interprête.
            </p>
            <p class="text-xl text-gray-700 mt-5">
                Inspiré de voyages, de rencontres et d’amitiés, Gilles Le Cornec
                vous propose ici un aperçu de son univers poétique et déjanté.
            </p>
        </div>
    </div>

    <div class="max-w-xl xl:w-1/2 xl:max-w-full mx-auto xl:mx-0">
        <img class="object-cover cropped-1 w-full" src="hero2.jpg" alt="" />
    </div>
</div>

<div
    class="relative inline-flex flex-col-reverse xl:flex-row xl:flex w-full pt-10 xl:pt-0"
>
    <div class="max-w-xl xl:w-1/2 xl:max-w-full mx-auto xl:mx-0">
        <img class="object-cover cropped-2 w-full" src="hero3.jpg" alt="" />
    </div>
    <div class="max-w-xl p-10 m-auto">
        <h1 class="relative -left-1 tracking-tight font-extrabold text-6xl">
            <span class="text-red-700">Kergann</span>
            <span class="text-gray-900">Le Cornec</span>
        </h1>
        <p class="text-xl text-gray-700 mt-5">
            Originaire des Côtes d’Armor, où il a été formé musicalement,
            Kergann Le Cornec est musicien et interprête.
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
