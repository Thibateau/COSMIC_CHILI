<template>
  <header class="bg-white">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8" aria-label="Top">
      <div class="w-full py-6 flex items-center justify-between border-b border-white lg:border-none">
        <div class="flex items-center">
          <a href="#">
            <span class="sr-only">Spicy-Rocket</span>
            <img class="h-10 w-auto" src="/images/logochili.png" alt="" />
          </a>
          <div class="hidden ml-10 space-x-8 lg:block">
            <a v-for="link in navigation" :key="link.name" :href="link.href" class="text-base font-medium text-black hover:text-green-500">
              {{ link.name }}
            </a>
          </div>
        </div>
            <div class="flex justify-center mt-6 lg:flex lg:mt-0 lg:-mx-2">
                <a href="#" class="mx-2 text-gray-600 transition-colors duration-200 transform dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300" aria-label="Reddit">
                <img class="w-6 h-6" src="/images/fb.gif">
                </a>
                <a href="#" class="mx-2 text-gray-600 transition-colors duration-200 transform dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300" aria-label="Reddit">
                <img class="w-6 h-6" src="/images/insta.gif">
                </a>
                <a href="#" class="mx-2 text-gray-600 transition-colors duration-200 transform dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300" aria-label="Reddit">
                <img class="w-6 h-6" src="/images/twitter.gif">
                </a>
            </div>
      </div>
      <div class="py-4 flex flex-wrap justify-center space-x-6 lg:hidden">
        <a v-for="link in navigation" :key="link.name" :href="link.href" class="text-base font-medium text-black hover:text-green-500">
          <RouterLink
          :to="{name: link.href}"
          :aria-label="link.name"
          :title="link.name">
                    {{ link.name }}
          </RouterLink>
        </a>
      </div>
    </nav>
  </header>
</template>

<script setup>
const navigation = [
  { name: 'Produits', href: 'products'},
  { name: 'Vos avis', href: 'notice'},
  { name: 'Goodies', href: 'goodies'},
]
</script>