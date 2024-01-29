<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20 border-b border-gray-100">
        <!-- Section header -->
        <div class="pb-12 md:pb-20">
          <h2 class="h2 font-cabinet-grotesk text-yellow-400">FAQs</h2>
        </div>

        <!-- Columns -->
        <div class="md:flex md:space-x-12 space-y-8 md:space-y-0">
          <!-- Column -->
          <div class="w-full space-y-8">
            <!-- Item -->
            <div class="space-y-2" v-for="i in 10" :key="i">
              <h4 class="text-xl font-cabinet-grotesk font-bold">
                Who is the best boss in the world?
              </h4>
              <p class="text-gray-200">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore magna aliqua, ut
                enim ad minim veniam. ALBANO
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Faqs",
};
</script>
