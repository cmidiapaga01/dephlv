<template>
  <div className="flex flex-col min-h-screen overflow-hidden">
    <!-- Site header -->
    <Header />

    <!-- Page content -->
    <main class="grow">
      <Hero />
      <Carousel />
      <Testimonials />
      <Blog />
      <Inspiration />
      <Cta />
      <Faqs />
      <!-- <Inspiration />
        <Creatives />
      <Carousel />
      <Creatives />
      <Pricing />
      <Testimonials />
      <Faqs />
      <Blog />
      <Cta /> -->
    </main>

    <!-- Site footer -->
    <Footer />
  </div>
</template>

<script>
import Header from "../partials/Header.vue";
import Hero from "../partials/Hero.vue";
import Inspiration from "../partials/Inspiration.vue";
import Carousel from "../partials/Carousel.vue";
import Creatives from "../partials/Creatives.vue";
import Pricing from "../partials/Pricing.vue";
import Testimonials from "../partials/Testimonials.vue";
import Faqs from "../partials/Faqs.vue";
import Blog from "../partials/Blog.vue";
import Cta from "../partials/Cta.vue";
import Footer from "../partials/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    Hero,
    Inspiration,
    Carousel,
    Creatives,
    Pricing,
    Testimonials,
    Faqs,
    Blog,
    Cta,
    Footer,
  },
};
</script>
