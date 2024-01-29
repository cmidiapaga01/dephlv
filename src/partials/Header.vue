<template>
  <header class="absolute w-full z-30 pt-4">
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="flex items-center justify-between h-16 md:h-20">
        <!-- Site branding -->
        <div class="shrink-0 mr-4">
          <!-- Logo -->
          <router-link class="block group" to="/" aria-label="Cruip">
            <img src="../images/logo.png" alt="" style="width: 150px" />
          </router-link>
        </div>

        <!-- Desktop navigation -->
        <nav class="flex grow">
          <!-- Desktop sign in links -->
          <ul class="flex grow justify-end flex-wrap items-center">
            <!-- <li>
              <router-link
                class="font-medium text-gray-600 decoration-blue-500 decoration-2 underline-offset-2 hover:underline px-3 lg:px-5 py-2 flex items-center transition duration-150 ease-in-out"
                to="/signin"
                >Sign in</router-link
              >
            </li> -->
            <li
              class="invisible sm:invisible md:invisible lg:visible xl:visible ml-3"
            >
              <book-button />
            </li>
            <li
              class="invisible sm:invisible md:invisible lg:visible xl:visible ml-3"
            >
              <InstaButton />
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
import BookButton from "./BookButton.vue";
import InstaButton from "./InstaButton.vue";
export default {
  name: "Header",
  components: { BookButton, InstaButton },
};
</script>
