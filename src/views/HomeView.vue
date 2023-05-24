<template>
  <swiper
    :slidesOffsetAfter="247"
    :slidesOffsetBefore="268"
    :slidesPerView="1.5"
    :spaceBetween="20"
    :slidesPerGroup="1"
    :loop="true"
    :loopFillGroupWithBlank="true"
    :modules="modules"
    navigation
    :pagination="{ clickable: true }"
    :scrollbar="{ draggable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    style="
      position: relative;
      overflow: hidden;
      list-style: none;
      padding: 0 0 35px;
      z-index: 1;
    "
  >
    <swiper-slide>
      <img
        style="
          width: 100%;
          height: 500px;
          box-shadow: 2px 10px 20px black;
          border-radius: 25px;
        "
        src="../assets/CODE-CLUB-SAMPLE-WEBSITE/Code-club-ent-copy.png"
      />
    </swiper-slide>
    <swiper-slide>
      <img
        style="
          width: 100%;
          height: 500px;
          box-shadow: 2px 10px 20px black;
          border-radius: 25px;
        "
        src="../assets/CODE-CLUB-SAMPLE-WEBSITE/IMG_2619.jpg"
      />
    </swiper-slide>
    <swiper-slide>
      <img
        style="
          width: 100%;
          height: 500px;
          box-shadow: 2px 10px 20px black;
          border-radius: 25px;
        "
        src="../assets/CODE-CLUB-SAMPLE-WEBSITE/IMG_2758.jpg"
      />
    </swiper-slide>
    <swiper-slide>
      <img
        style="
          width: 100%;
          height: 500px;
          box-shadow: 2px 10px 20px black;
          border-radius: 25px;
        "
        src="../assets/CODE-CLUB-SAMPLE-WEBSITE/IMG_2765.jpg"
      />
    </swiper-slide>
    <swiper-slide>
      <img
        style="
          width: 100%;
          height: 500px;
          box-shadow: 2px 10px 20px black;
          border-radius: 25px;
        "
        src="../assets/CODE-CLUB-SAMPLE-WEBSITE/IMG_3360.jpg"
      />
    </swiper-slide>
    <div class="parallax-slider-navigation">
      <div class="nav-indicator nextArrow ">
        <font-awesome-icon icon="fa-solid fa-chevron-right"  />
      </div>

      <div class="nav-indicator prevArrow ">
        <font-awesome-icon icon="fa-solid fa-chevron-left" />
      </div>
    </div>
  </swiper>
</template>
<script>
// import Swiper core and required modules
import { Navigation, Pagination, A11y } from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { FontAwesomeLayersText } from "@fortawesome/vue-fontawesome";
// Import Swiper styles
export default {
  components: {
    Swiper,
    SwiperSlide,
    FontAwesomeIcon,
    FontAwesomeLayersText,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Navigation, Pagination, A11y],
      // Default parameters
      slidesPerView: 1,
      spaceBetween: 10,
      // Responsive breakpoints
      breakpoints: {
        // when window width is >= 320px
        120: {
          slidesPerView: 1,
          spaceBetween: 10,
        },
        120: {
          slidesPerView: 1,
          spaceBetween: 20,
        },
        320: {
          slidesPerView: 1,
          spaceBetween: 20,
        },
        620: {
          slidesPerView: 1,
          spaceBetween: 20,
        },

        900: {
          slidesOffsetAfter: 200,
          slidesOffsetBefore: 200,
          slidesPerView: 1,
          spaceBetween: 20,
          speed: 400,
        },
      },
    };
  },
};
</script>
<style>
swiper-slide {
  height: 250px;
  background-color: silver;
}
img {
  width: 100%;
  height: 100%;
}
.swiper-button-next::after {
  
  padding-right: 150px;
}

.swiper-button-prev::after {
  padding-left: 150px;
}
.swiper-button-next::after,
.swiper-button-prev::after {
  font-size: 14rem !important;
  color: rgba(255, 255, 255, 0.75);
}
.swiper-pagination {
  bottom: 35px !important;

  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-pagination-bullet,
.ahmed {
  width: 1rem;
  height: 1rem;
  background-color: rgba(255, 255, 255, 0.75);
}

.swiper-pagination-bullet-active,
.ahmed-active {
  width: 0.8rem;
  height: 0.8rem;
  opacity: 1;
  background-color: white;
  border: 1px solid #373636;
}
</style>
