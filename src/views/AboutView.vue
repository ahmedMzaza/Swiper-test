<template>
  <div class="gallery" style="width: 500px;">
    <div class="gallery-section" v-for="gallery in galleries" v-bind:key="gallery.name">
      <div v-if="gallery.category == false">
        <h2>{{ gallery.tittle }}</h2>
        <Swiper
        :loop="true"
          :effect="'coverflow'"
          :grab-cursor="true"
          :centered-slides="true"
          :slides-per-view="'auto'"
          :autoplay="{ delay: 2500, disbleonInteraction: false ,}"
          :coverflow-effect="{
            rotate: 50,
            stretch: 0,
            depth: 100,
            modifier: 1,
            slideShadows: true,
          }"
          :pagination="true"
          :modules="modules"
          class="mySwiper"
        >
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
          <SwiperSlide>
            <img src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png" />
          </SwiperSlide>
        </Swiper>
      </div>
    </div>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination, EffectCoverflow } from "swiper";
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/navigation";
import "swiper/css/pagination";
export default {
  name: "CarouselVue",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [EffectCoverflow, Autoplay, Pagination],
      galleries: [
        {
          name: "THE code Gallery",
          category: false,
          tittle: "category using vue ",
          images: {
            photo01: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Code-club-ent-copy.png",
            photo02: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png",
            photo03: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png",
            photo04: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png",
            photo05: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png",
            photo06: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png",
            photo07: "../assets/CODE-CLUB-SAMPLE-WEBSITE/Untitled-2.png",
          },
        },
      ],
    };
  },
};
</script>
<style scoped>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.gallery .gallery-section {
  background: #424242;
  border-radius: 10px;
  height: auto;
  margin: 5% 0 8% 0;
}
h2 {
  color: #ffffff;
  font-weight: 500;
  max-width: 0 1% 0 0%;
  padding: 1%;
  text-align: center;
  text-transform: uppercase;
}

.gallery-section .swiper {
  padding-top: 50px;
  width: 100%;

  padding-bottom: 50px;
}

.gallery-section .swiper-slide img {
  display: block;
  width: 100%;
}
</style>
