<template>
  <div class="h-full justify-between">
    <header class="h-24 sm:h-24 flex items-center z-30 w-full">
      <div class="container mx-auto px-6 flex items-center justify-between">
        <div class="text-green-400 font-semibold text-3xl">Raffil.io</div>
        <div class="flex items-center">
          <nav class="uppercase text-lg lg:flex items-center hidden">
            <NuxtLink to="/" class="py-2 px-6 flex"> Home </NuxtLink>
            <NuxtLink to="/about" class="py-2 px-6 flex"> About </NuxtLink>
            <NuxtLink to="/contact" class="py-2 px-6 flex"> Contact </NuxtLink>
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
          </nav>
          <Menu as="div" class="lg:hidden ml-3 relative">
            <div>
              <MenuButton
                class="
                  flex
                  text-sm
                "
              >
                <span class="sr-only">Open user menu</span>
                <div class="space-y-2">
                  <div class="w-8 h-0.5 bg-gray-600"></div>
                  <div class="w-8 h-0.5 bg-gray-600"></div>
                  <div class="w-8 h-0.5 bg-gray-600"></div>
                </div>
              </MenuButton>
            </div>
            <transition
              enter-active-class="transition ease-out duration-100"
              enter-from-class="transform opacity-0 scale-95"
              enter-to-class="transform opacity-100 scale-100"
              leave-active-class="transition ease-in duration-75"
              leave-from-class="transform opacity-100 scale-100"
              leave-to-class="transform opacity-0 scale-95"
            >
              <MenuItems
                class="
                  origin-top-right
                  absolute
                  right-0
                  mt-2
                  w-48
                  rounded-md
                  shadow-lg
                  py-1
                  bg-white
                  ring-1 ring-black ring-opacity-5
                  focus:outline-none
                "
              >
                <MenuItem v-slot="{ active }">
                  <a
                    href="/"
                    :class="[
                      active ? 'bg-gray-100' : '',
                      'block px-4 py-2 text-sm text-gray-700',
                    ]"
                    >Home</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="/about"
                    :class="[
                      active ? 'bg-gray-100' : '',
                      'block px-4 py-2 text-sm text-gray-700',
                    ]"
                    >About</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="/contact"
                    :class="[
                      active ? 'bg-gray-100' : '',
                      'block px-4 py-2 text-sm text-gray-700',
                    ]"
                    >Contact</a
                  >
                </MenuItem>
                <MenuItem v-slot="{ active }">
                  <a
                    href="#"
                    :class="[
                      active ? 'bg-gray-100' : '',
                      'block px-4 py-2 text-sm text-gray-700',
                    ]"
                    >App</a
                  >
                </MenuItem>
              </MenuItems>
            </transition>
          </Menu>
        </div>
      </div>
    </header>
    <slot />
    <footer
      class="
        p-4
        md:flex md:items-center md:justify-between md:p-6
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


<script setup>
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Menu,
  MenuButton,
  MenuItem,
  MenuItems,
} from "@headlessui/vue";
definePageMeta({
  name: "main",
});
</script>
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
