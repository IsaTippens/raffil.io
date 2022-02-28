<template>
  <div class="h-full justify-between">
    <header class="h-24 sm:h-24 flex items-center z-30 w-full">
      <div class="container mx-auto px-6 flex items-center justify-between">
        <div class="text-green-400 font-semibold text-3xl">Raffil.io</div>
        <div class="flex items-center">
          <nav
            class="
              dark:text-white
              uppercase
              text-lg
              lg:flex
              items-center
              hidden
            "
          >
            <NuxtLink to="/" class="py-2 px-6 flex"> Home </NuxtLink>
            <NuxtLink to="/about" class="py-2 px-6 flex"> About </NuxtLink>
            <NuxtLink to="/contact" class="py-2 px-6 flex"> Contact </NuxtLink>
            <NuxtLink to="/app" class="py-2 px-6 flex bg-gradient-to-r
          from-blue-100
          to-green-100 rounded-full text-green-400 drop-shadow">App</NuxtLink>
          </nav>
          <button class="lg:hidden flex flex-col ml-4">
            <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1"> </span>
            <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1"> </span>
            <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1"> </span>
          </button>
        </div>
      </div>
    </header>
    <Nuxt />
    <footer
      class="
        p-4
        md:flex md:items-center md:justify-between md:p-6
        dark:bg-gray-800
      "
    >
      <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400"
        >© {{ year }}
        <a href="https://flowbite.com" class="hover:underline" target="_blank"
          >Raffil.io</a
        >. All Rights Reserved.
      </span>
      <ul class="flex flex-wrap items-center mt-3 sm:mt-0">
        <li>
          <a
            href="#"
            class="
              mr-4
              text-sm text-gray-500
              hover:underline
              md:mr-6
              dark:text-gray-400
            "
            >About</a
          >
        </li>
        <li>
          <a
            href="#"
            class="
              mr-4
              text-sm text-gray-500
              hover:underline
              md:mr-6
              dark:text-gray-400
            "
            >Privacy Policy</a
          >
        </li>
        <li>
          <a
            href="#"
            class="
              mr-4
              text-sm text-gray-500
              hover:underline
              md:mr-6
              dark:text-gray-400
            "
            >Licensing</a
          >
        </li>
        <li>
          <a
            href="#"
            class="text-sm text-gray-500 hover:underline dark:text-gray-400"
            >Contact</a
          >
        </li>
      </ul>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      year: new Date().getFullYear(),
    };
  },
  mounted() {},
};
</script>
