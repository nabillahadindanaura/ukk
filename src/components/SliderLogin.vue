<template>
  <swiper
    :pagination="true"
    draggable="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    @autoplayTimeLeft="onAutoplayTimeLeft"
    auto
    grab-cursor="true"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide>
      <div
        class="bg-asset w-100 h-100"
        style="background: url('/src/assets/img/posterB.jpg')"
      ></div>
    </swiper-slide>

    <swiper-slide>
      <div
        class="bg-asset w-100 h-100"
        style="background: url('/src/assets/img/girlBakery2.jpg')"
      ></div>
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import required modules
import { Autoplay, Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Autoplay],
    };
  },
};
</script>
<style lang="scss">
.swiper {
  min-height: 100vh;
}
.bg-asset {
  background-repeat: no-repeat !important;
  background-size: cover !important;
  background-position: center !important;
}
</style>
