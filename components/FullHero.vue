<template>
    <div class="w-full bg-center bg-cover h-[32rem]" style="background-image: url(images/chili.jpg);">
        <div class="flex items-center justify-center w-full h-full">
            <div class="text-center">
                <h1 class="text-2xl font-semibold text-white uppercase lg:text-3xl">Découvrez nos <span class="text-green-600">RECETTES</span></h1>
                <RouterLink
                :to="{name: 'products'}">
                <button class="w-full px-4 py-2 mt-4 text-sm font-medium text-white uppercase transition-colors duration-200 transform bg-green-600 rounded-md lg:w-auto hover:bg-green-500 focus:outline-none focus:bg-green-600">Voir nos produits</button>
                </RouterLink>
            </div>
        </div>
    </div>
</template>