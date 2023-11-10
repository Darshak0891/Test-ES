<template>
  <div class="edu-blog blog-style-4">
    <div class="inner">
      <div class="thumbnail">
        <div class="blog-gallery-activation" v-if="blogInfo.slider">
          <swiper
            class="swiper"
            :modules="modules"
            :slidesPerView="1"
            :loop="true"
            :spaceBetween="0"
            :autoplay="{
              delay: 3000,
              disableOnInteraction: false,
            }"
            :navigation="{
              nextEl: '.swiper-btn-nxt',
              prevEl: '.swiper-btn-prv',
            }"
            :speed="1000"
            :grabCursor="true"
          >
            <swiper-slide v-for="(sliderThumb, i) in blogInfo.slider" :key="i">
              <NuxtLink to="/blog/blog-details">
                <img
                  :src="'/images/blog/blog-standard/' + sliderThumb"
                  :alt="blogInfo.alt"
                />
              </NuxtLink>
            </swiper-slide>
          </swiper>
          <div class="swiper-navigation">
            <div class="swiper-btn-nxt">
              <i class="icon-west"></i>
            </div>
            <div class="swiper-btn-prv">
              <i class="icon-east"></i>
            </div>
          </div>
        </div>

        <NuxtLink to="/blog/blog-details" v-else>
          <img
            :src="'/images/blog/blog-standard/' + blogInfo.imgSrc"
            :alt="blogInfo.alt"
          />
        </NuxtLink>
      </div>
      <div class="content">
        <div class="category-wrap">
          <NuxtLink to="/blog/blog-masonry" class="blog-category">{{
            blogInfo.category
          }}</NuxtLink>
        </div>
        <h3 class="title">
          <NuxtLink to="/blog/blog-details">{{ blogInfo.title }}</NuxtLink>
        </h3>
        <ul class="blog-meta">
          <li><i class="icon-27"></i>{{ blogInfo.date }}</li>
          <li><i class="icon-28"></i>{{ blogInfo.comment }}</li>
        </ul>
        <p>{{ blogInfo.excerpt3 }}</p>
        <div class="read-more-btn">
          <Button class="edu-btn btn-border btn-medium">
            Download <i class="icon-4"></i>
          </Button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Autoplay } from "swiper";
import { Navigation } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";

export default {
  props: ["blogInfo"],
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Navigation],
    };
  },
  methods: {
    handleVideoPopup() {
      this.$refs.video_modal.playVideo();
    },
  },
};
</script>

<style>
.blog-gallery-activation {
  position: relative;
}

.video-area-1 .video-play-btn {
  cursor: pointer;
}
</style>
