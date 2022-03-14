<template>
  <div class="h-full justify-between">
    <nav class="w-full">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <div class="text-green-400 font-semibold text-3xl">Raffil.io</div>
          <div class="flex items-center">
            <div
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
              <NuxtLink to="/contact" class="py-2 px-6 flex">
                Contact
              </NuxtLink>
              <NuxtLink
                to="/app"
                class="
                  py-2
                  px-6
                  flex
                  bg-gradient-to-r
                  from-blue-100
                  to-green-100
                  rounded-full
                  text-green-400
                  drop-shadow
                "
                >App</NuxtLink
              >
            </div>

            <button
              @click="toggle"
              class="md:hidden flex flex-col ml-4 focus:outline-none"
            >
              <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1"> </span>
              <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1"> </span>
              <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1"> </span>
            </button>
          </div>
        </div>
      </div>
      <div :class="[isOpen ? '' : 'hidden', 'md:hidden']">
        <div class="px-2 pt-2 pb-3 sm:px-3">
          <NuxtLink
            to="/"
            class="
              block
              px-3
              py-2
              rounded-md
              text-base
              font-medium
              bg-green-400
              focus:outline-none focus:bg-green-200
            "
            >Home</NuxtLink
          >
          <NuxtLink
            to="/about"
            class="
              mt-1
              block
              px-3
              py-2
              rounded-md
              text-base
              font-medium
              hover:bg-green-200
              focus:outline-none focus:bg-green-200
            "
            >About</NuxtLink
          >
          <NuxtLink
            to="/contact"
            class="
              mt-1
              block
              px-3
              py-2
              rounded-md
              text-base
              font-medium
              hover:bg-green-200
              focus:outline-none focus:bg-green-200
            "
            >Contact</NuxtLink
          >
        </div>
        <div class="px-2 pt-2 pb-3 border-t border-gray-700">
          <NuxtLink
            to="/app"
            class="
              mt-1
              block
              px-3
              py-2
              rounded-md
              text-base
              font-medium
              hover:bg-green-200
              focus:outline-none focus:bg-green-200
            "
            >App</NuxtLink
          >
        </div>
      </div>
    </nav>
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
      isOpen: false,
      year: new Date().getFullYear(),
    };
  },
  mounted() {},
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>
