<template>
  <div class="">
    <!--Banner-->
    <div class="">
      <div
        class="w-full h-full bg-gradient-to-r from-blue-100 to-green-200 p-8"
      >
        <div class="max-w-7xl mx-auto text-center">
          <p
            class="
              text-3xl text-green-400
              font-semibold
              tracking-wide
              uppercase
            "
          >
            Raffil.io
          </p>
          <p
            class="
              text-base text-green-400
              font-semibold
              tracking-wide
              uppercase
            "
          >
            A zero loss, zero risk DAPP
          </p>
          <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
            Lorem ipsum dolor sit amet consect adipisicing elit. Possimus magnam
            voluptatum cupiditate veritatis in accusamus quisquam.
          </p>
        </div>
      </div>
    </div>
    <!--Banner End-->
    <!--Body-->
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="mt-10">
        <div class="grid md:grid-cols-2 gap-4">
          <div class="w-full">
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
              maximus justo sit amet mauris tristique sollicitudin. Curabitur ut
              ante auctor, feugiat dolor non, mollis justo. Praesent fringilla
              gravida diam a condimentum. Etiam hendrerit et velit sed rhoncus.
              Nullam gravida sit amet nulla nec cursus. Duis aliquam arcu
              ligula, sollicitudin gravida odio porta sit amet. Nullam venenatis
              pretium justo, suscipit laoreet turpis ornare non. Nunc hendrerit
              varius sem, vel placerat erat lacinia at. In sit amet lorem sed
              sapien iaculis vehicula. Pellentesque habitant morbi tristique
              senectus et netus et malesuada fames ac turpis egestas. Nullam ut
              sagittis mi. Sed consectetur sit amet mi non porttitor. Nullam
              nibh tellus, ornare a nunc sit amet, hendrerit hendrerit augue.
            </p>
          </div>
          <div
            class="
              w-full
              p-4
              bg-gradient-to-r
              from-blue-100
              to-green-200
              rounded
            "
          >
            <div class="mt-5 md:mt-0 md:col-span-2">
              <!--FORM-->
              <form action="#" method="POST">
                <div class="shadow sm:rounded-md sm:overflow-hidden">
                  <div class="px-4 py-5 bg-white space-y-6 sm:p-6">
                    <div class="grid grid-cols-3 gap-6">
                      <div class="col-span-3 sm:col-span-2">
                        <label
                          for="company-website"
                          class="block text-sm font-medium text-gray-700"
                        >
                          Website
                        </label>
                        <div class="mt-1 flex rounded-md shadow-sm">
                          <span
                            class="
                              inline-flex
                              items-center
                              px-3
                              rounded-l-md
                              border border-r-0 border-gray-300
                              bg-gray-50
                              text-gray-500 text-sm
                            "
                          >
                            http://
                          </span>
                          <input
                            type="text"
                            name="company-website"
                            id="company-website"
                            class="
                              focus:ring-indigo-500 focus:border-indigo-500
                              flex-1
                              block
                              w-full
                              rounded-none rounded-r-md
                              sm:text-sm
                              border-gray-300
                            "
                            placeholder="www.example.com"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="col-span-6 sm:col-span-3">
                      <label
                        for="items"
                        class="block text-sm font-medium text-gray-700"
                        >Dropdown Menu</label
                      >
                      <select
                        id="items"
                        name="items"
                        autocomplete="country-name"
                        class="
                          mt-1
                          block
                          w-full
                          py-2
                          px-3
                          border border-gray-300
                          bg-white
                          rounded-md
                          shadow-sm
                          focus:outline-none
                          focus:ring-indigo-500
                          focus:border-indigo-500
                          sm:text-sm
                        "
                      >
                        <option>Item 1</option>
                        <option>Item 2</option>
                        <option>Item 3</option>
                      </select>
                    </div>
                    <div>
                      <label
                        for="about"
                        class="block text-sm font-medium text-gray-700"
                      >
                        About
                      </label>
                      <div class="mt-1">
                        <textarea
                          id="about"
                          name="about"
                          rows="3"
                          class="
                            shadow-sm
                            focus:ring-indigo-500 focus:border-indigo-500
                            mt-1
                            block
                            w-full
                            sm:text-sm
                            border border-gray-300
                            rounded-md
                          "
                          placeholder="you@example.com"
                        />
                      </div>
                      <p class="mt-2 text-sm text-gray-500">
                        Brief description for your profile. URLs are
                        hyperlinked.
                      </p>
                    </div>
                  </div>
                </div>
              </form>
              <!--FORM END-->
            </div>
          </div>
        </div>
        <div class="">
          <p>
            Phasellus non erat a enim porttitor sollicitudin. In dapibus ligula
            vitae scelerisque ornare. Vestibulum non quam vitae sem varius
            pulvinar at vitae mauris. Praesent sem velit, dapibus id luctus in,
            porta sit amet elit. Duis nec odio placerat, scelerisque neque non,
            consequat velit. In quis tellus at nulla blandit vulputate. Nam in
            metus consequat, gravida nulla et, volutpat justo. Praesent eu
            laoreet mauris.
          </p>
        </div>
      </div>
    </div>
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
</script>
<script>
definePageMeta({
  layout: "main",
});
export default {
  name: "IndexPage",
};
</script>
