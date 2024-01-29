<template>
  <section class="bg-red-900 mt-10">
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
          <h2 class="h2 font-cabinet-grotesk text-yellow-400">Feel at home</h2>
          <h2 class="h4 font-cabinet-grotesk text-gray-300 mt-2 mb-4">
            Our modern hostel provides you with everything you need to enjoy
            your stay in a chill and cozy atmosphere
          </h2>
          <BookButton />
        </div>

        <!-- Carousel built with Swiper.js [https://swiperjs.com/] -->
        <!-- * Custom styles in src/css/additional-styles/theme.scss -->
        <div class="carousel swiper-container max-w-sm mx-auto sm:max-w-none">
          <div class="swiper-wrapper">
            <!-- Carousel items -->
            <div
              class="swiper-slide h-auto flex flex-col"
              v-for="i in 60"
              :key="i"
            >
              <!-- Image -->
              <button>
                <img
                  class="w-full aspect-[7/4] object-cover"
                  :src="`/photos/prod/HastaLaVista-${i + 1}.jpg`"
                  width="259"
                  height="259"
                  alt="Carousel 01"
                  @click="onShowDetail(i)"
                />
              </button>
              <!-- White box -->
            </div>
          </div>
        </div>

        <!-- Arrows -->
        <div class="flex mt-12 space-x-4 justify-end">
          <button
            class="carousel-prev relative z-20 w-14 h-14 rounded-full flex items-center justify-center group bg-gray-700 hover:bg-yellow-500 transition duration-150 ease-in-out"
          >
            <span class="sr-only">Previous</span>
            <svg
              class="w-4 h-4 fill-gray-400 group-hover:fill-white transition duration-150 ease-in-out"
              viewBox="0 0 16 16"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M6.7 14.7l1.4-1.4L3.8 9H16V7H3.8l4.3-4.3-1.4-1.4L0 8z" />
            </svg>
          </button>
          <button
            class="carousel-next relative z-20 w-14 h-14 rounded-full flex items-center justify-center group bg-gray-700 hover:bg-yellow-500 transition duration-150 ease-in-out"
          >
            <span class="sr-only">Next</span>
            <svg
              class="w-4 h-4 fill-gray-400 group-hover:fill-white transition duration-150 ease-in-out"
              viewBox="0 0 16 16"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9.3 14.7l-1.4-1.4L12.2 9H0V7h12.2L7.9 2.7l1.4-1.4L16 8z"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
    <div id="image-viewer" v-if="showDetail">
      <span class="close" @click="showDetail = false">&times;</span>
      <img
        :src="`/photos/prod/HastaLaVista-${currentImage + 1}.jpg`"
        class="modal-content"
        id="full-image"
      />
      <div class="flex mt-12 space-x-4 justify-center">
        <button
          class="carousel-prev relative z-20 w-14 h-14 rounded-full flex items-center justify-center group bg-gray-700 hover:bg-yellow-500 transition duration-150 ease-in-out"
          @click="previous"
        >
          <span class="sr-only">Previous</span>
          <svg
            class="w-4 h-4 fill-gray-400 group-hover:fill-white transition duration-150 ease-in-out"
            viewBox="0 0 16 16"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path d="M6.7 14.7l1.4-1.4L3.8 9H16V7H3.8l4.3-4.3-1.4-1.4L0 8z" />
          </svg>
        </button>
        <button
          class="carousel-next relative z-20 w-14 h-14 rounded-full flex items-center justify-center group bg-gray-700 hover:bg-yellow-500 transition duration-150 ease-in-out"
          @click="next"
        >
          <span class="sr-only">Next</span>
          <svg
            class="w-4 h-4 fill-gray-400 group-hover:fill-white transition duration-150 ease-in-out"
            viewBox="0 0 16 16"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M9.3 14.7l-1.4-1.4L12.2 9H0V7h12.2L7.9 2.7l1.4-1.4L16 8z"
            />
          </svg>
        </button>
      </div>
      <div class="mx-auto text-center pt-10">
        <BookButton />
      </div>
    </div>
  </section>
</template>

<script>
// Import Swiper
import Swiper, { Navigation } from "swiper";
import "swiper/css";
import BookButton from "./BookButton.vue";
Swiper.use([Navigation]);

export default {
  name: "Carousel",
  data() {
    return {
      showDetail: false,
      currentImage: 0,
    };
  },
  mounted() {
    // eslint-disable-next-line no-unused-vars
    const carousel = new Swiper(".carousel", {
      breakpoints: {
        320: {
          slidesPerView: 1,
        },
        640: {
          slidesPerView: 2,
        },
        1024: {
          slidesPerView: 4,
        },
      },
      grabCursor: true,
      loop: false,
      centeredSlides: false,
      initialSlide: 0,
      spaceBetween: 24,
      watchSlidesProgress: true,
      navigation: {
        nextEl: ".carousel-next",
        prevEl: ".carousel-prev",
      },
    });
  },
  components: { BookButton },
  methods: {
    onShowDetail(index) {
      this.showDetail = true;
      this.currentImage = index;
    },
    next() {
      if (this.currentImage <= 59) {
        this.currentImage++;
      } else {
        this.currentImage = 0;
      }
    },
    previous() {
      if (this.currentImage == 0) {
        this.currentImage = 59;
      } else {
        this.currentImage--;
      }
    },
  },
};
</script>

<style>
/* Style the Image Used to Trigger the Modal */
/* img {
    border-radius: 5px;
    cursor: pointer;
    transition: 0.3s;
}

img:hover {opacity: 0.7;} */

/* The Modal (background) */
#image-viewer {
  position: fixed;
  z-index: 120;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.9);
}
.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
}
.modal-content {
  animation-name: zoom;
  animation-duration: 0.6s;
}
@keyframes zoom {
  from {
    transform: scale(0);
  }
  to {
    transform: scale(1);
  }
}
#image-viewer .close {
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
}
#image-viewer .close:hover,
#image-viewer .close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

@media only screen and (max-width: 700px) {
  .modal-content {
    width: 100%;
  }
}
</style>
