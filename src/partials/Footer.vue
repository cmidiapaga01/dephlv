<template>
  <footer>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-8 md:py-12">
        <!-- Top area -->
        <div
          class="flex flex-col sm:flex-row items-center justify-center sm:justify-between mb-12 md:mb-6"
        >
          <div class="shrink-0 mr-4">
            <img src="../images/logo.png" alt="" style="width: 150px" />
          </div>
          <div>
            <book-button class="mb-4" />
            <insta-button />
          </div>
        </div>

        <!-- Bottom area -->
        <div
          class="text-center md:flex md:items-center md:justify-between mb-8 md:mb-6"
        >
          <!-- Social links -->

          <!-- Left links -->
          <!-- <div class="text-sm font-medium md:order-1 space-x-6 mb-2 md:mb-0">
            <a
              class="text-gray-500 decoration-yellow-500 decoration-2 underline-offset-2 hover:underline"
              href="#0"
              >About</a
            >
            <a
              class="text-gray-500 decoration-yellow-500 decoration-2 underline-offset-2 hover:underline"
              href="#0"
              >Get in touch</a
            >
            <a
              class="text-gray-500 decoration-yellow-500 decoration-2 underline-offset-2 hover:underline"
              href="#0"
              >Privacy &amp; Terms</a
            >
          </div> -->
        </div>

        <!-- Bottom notes -->
        <div class="text-xs text-gray-400 text-center md:text-left">
          Hostel Hasta la Vista is concepted as a home away from home for
          students, youngsters and explorers. Our aim is to creat a warm
          environment with convenient prices. something wrong here or you would
          like to have it removed, please
          <a
            class="font-medium text-yellow-400 decoration-yellow-400 underline-offset-2 hover:underline"
            href="mailto:contacto@hhlv.com"
            target="_blank"
            >contact us</a
          >.
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import BookButton from "./BookButton.vue";
import InstaButton from "./InstaButton.vue";

export default {
  name: "Footer",
  components: { BookButton, InstaButton },
};
</script>
