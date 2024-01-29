<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20">
        <!-- Section header -->
        <div class="pb-12 md:pb-20">
          <h2
            class="h2 font-cabinet-grotesk text-center md:text-left text-yellow-400"
          >
            What to do in Sarandë
          </h2>
        </div>
        <!-- Slider main container -->
        <div class="blog-carousel swiper-container">
          <!-- Additional required wrapper -->
          <div class="swiper-wrapper">
            <!-- Slides -->
            <article
              v-for="i in 10"
              :key="i"
              class="swiper-slide max-w-xs w-40 h-70 bg-white m-4 flex flex-col p-4"
              data-aos="fade-down"
            >
              <img
                class="w-full aspect-[7/4] object-cover group-hover:scale-105 transition duration-700 ease-out"
                src="../images/blog-01.jpg"
                width="347"
                height="198"
                alt="Post 01"
              />
              <a class="text-xl text-yellow-400 my-2" href="#0">
                Slide {{ i }}
              </a>
              <p class="text-xs text-black">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Laborum, alias blanditiis rem.
              </p>
            </article>
          </div>
          <!-- If we need pagination -->
          <!-- <div class="mx-auto w-full text-center">
            <div class="blog-carousel-pagination"></div>
          </div> -->
        </div>
        <!-- Posts -->
        <!-- <div class="swiper blog-carousel swiper-container">
          <div class="swiper-wrapper">
    
            <div
              class="max-w-sm mx-auto md:max-w-none grid gap-12 md:grid-cols-3 md:gap-x-6 md:gap-y-8 items-start"
            >
              <div class="swiper-slide">
                <article
                  v-for="i in 10"
                  :key="i"
                  class="h-full flex flex-col space-y-5"
                  data-aos="fade-down"
                >
                  
                  <a class="block group overflow-hidden" href="#0">
                    <img
                      class="w-full aspect-[7/4] object-cover group-hover:scale-105 transition duration-700 ease-out"
                      src="../images/blog-01.jpg"
                      width="347"
                      height="198"
                      alt="Post 01"
                    />
                  </a>
                 
                  <div class="grow flex flex-col">
                    <header>
                      <h3 class="h4 font-cabinet-grotesk font-bold mb-2">
                        <a
                          class="inline-block decoration-blue-500 decoration-2 underline-offset-2 hover:underline"
                          href="#0"
                          >Concept Art & Illustrations by Stef Euphoria</a
                        >
                      </h3>
                    </header>
                    <p class="text-gray-500 grow">
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                      sed do eiusmod tempor incididunt ut labore et dolore.
                    </p>
                    <footer class="flex items-center text-sm mt-4">
                      <a href="#0">
                        <img
                          class="rounded-full shrink-0 mr-3"
                          src="../images/blog-author-01.jpg"
                          width="32"
                          height="32"
                          alt="Author 01"
                        />
                      </a>
                      <div>
                        <span class="text-gray-500">By</span>
                        <a
                          class="font-medium decoration-blue-500 decoration-2 underline-offset-2 hover:underline"
                          href="#0"
                          >Knut Mayer</a
                        >
                      </div>
                    </footer>
                  </div>
                </article>
              </div>
            </div>
          </div>
        </div>
        <div class="blog-carousel-pagination text-center"></div> -->
      </div>
    </div>
  </section>
</template>

<script>
import Swiper, { Pagination } from "swiper";
import "swiper/css";
import "swiper/css/pagination";
Swiper.use([Pagination]);
export default {
  name: "Blog",
  mounted() {
    // eslint-disable-next-line no-unused-vars
    const blog = new Swiper(".blog-carousel", {
      slidesPerView: 1,
      watchSlidesProgress: true,
      pagination: {
        el: ".blog-carousel-pagination",
        clickable: true,
      },
    });
  },
};
</script>

<style>
.swiper-pagination-bullet-active {
  background-color: #ffef0f !important;
}
.swiper-pagination-bullet {
  margin: 0 4px;
}
</style>
