<template>
    <div class="testimonial-area-4">
        <div class="container">
            <div class="row g-5">
                <div class="col-lg-5">
                    <div class="testimonial-heading-area">
                        <SectionTitle preTitle='Testimonials' preTitleClass='pre-textsecondary'
                            title='What Our Students Have To Say'
                            subTitle='Lorem ipsum dolor sit amet consectur adipiscing elit sed eiusmod tempor incididunt labore dolore magna aliquaenim ad minim.'
                            alignment='section-left' />
                    </div>
                    <div class="swiper-navigation">
                        <div class="swiper-btn-nxt">
                            <i class="icon-west"></i>
                        </div>
                        <div class="swiper-btn-prv">
                            <i class="icon-east"></i>
                        </div>
                    </div>
                </div>
                <div class="col-lg-7">
                    <div>
                        <swiper 
                            class="testimonial-activation-3" 
                            :modules="modules" 
                            :slidesPerView="1" 
                            :loop="true" 
                            :spaceBetween="0"
                            :autoplay="{
                                delay: 3000,
                                disableOnInteraction: false,
                            }"
                            :speed="1000" 
                            :grabCursor="true"
                            :navigation="{
                                clickable: true,
                                nextEl: '.swiper-btn-nxt',
                                prevEl: '.swiper-btn-prv',
                            }" 
                            :breakpoints="{
                                '577': {
                                    slidesPerView: 2,
                                },
                            }">
                            <swiper-slide>
                                <div class="testimonial-grid testimonial-style-3">
                                    <div class="thumbnail">
                                        <img src="/images/testimonial/testimonial-01.png" alt="Testimonial">
                                    </div>
                                    <div class="content">
                                        <p>Lorem ipsum dolor amet consec tur elit adicing sed do usmod zx tempor enim
                                            minim veniam quis nostrud exer citation.</p>
                                        <div class="rating-icon">
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                        </div>
                                        <h5 class="title">Ray Sanchez</h5>
                                        <span class="subtitle">Student</span>
                                    </div>
                                </div>
                            </swiper-slide>
                            <swiper-slide>
                                <div class="testimonial-grid testimonial-style-3">
                                    <div class="thumbnail">
                                        <img src="/images/testimonial/testimonial-02.png" alt="Testimonial">
                                    </div>
                                    <div class="content">
                                        <p>Lorem ipsum dolor amet consec tur elit adicing sed do usmod zx tempor enim
                                            minim veniam quis nostrud exer citation.</p>
                                        <div class="rating-icon">
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                        </div>
                                        <h5 class="title">Thomas Lopez</h5>
                                        <span class="subtitle">Designer</span>
                                    </div>
                                </div>
                            </swiper-slide>
                            <swiper-slide>
                                <div class="testimonial-grid testimonial-style-3">
                                    <div class="thumbnail">
                                        <img src="/images/testimonial/testimonial-03.png" alt="Testimonial">
                                    </div>
                                    <div class="content">
                                        <p>Lorem ipsum dolor amet consec tur elit adicing sed do usmod zx tempor enim
                                            minim veniam quis nostrud exer citation.</p>
                                        <div class="rating-icon">
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                        </div>
                                        <h5 class="title">Amber Page</h5>
                                        <span class="subtitle">Developer</span>
                                    </div>
                                </div>
                            </swiper-slide>
                            <swiper-slide>
                                <div class="testimonial-grid testimonial-style-3">
                                    <div class="thumbnail">
                                        <img src="/images/testimonial/testimonial-04.png" alt="Testimonial">
                                    </div>
                                    <div class="content">
                                        <p>Lorem ipsum dolor amet consec tur elit adicing sed do usmod zx tempor enim
                                            minim veniam quis nostrud exer citation.</p>
                                        <div class="rating-icon">
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                            <i class="icon-23"></i>
                                        </div>
                                        <h5 class="title">Robert Tapp</h5>
                                        <span class="subtitle">Content Creator</span>
                                    </div>
                                </div>
                            </swiper-slide>
                        </swiper>
                    </div>
                </div>
            </div>
        </div>
        <ul class="shape-group">
            <MouseMove addClassName="shape-1" dataDepth="2" imgSrc="/images/others/shape-18.png" />
            <li class="shape-2">
                <img src="/images/others/map-shape-3.png" alt="Shape">
            </li>
        </ul>
    </div>
</template>


<script>
import MouseMove from '../animation/MouseMove.vue';
import SectionTitle from '../common/SectionTitle.vue';
import { Autoplay, Navigation } from 'swiper'
import { Swiper, SwiperSlide } from "swiper/vue";

export default {
    components: {
        SectionTitle,
        MouseMove,
        Swiper,
        SwiperSlide
    },
    setup() {
        return {
            modules: [Autoplay, Navigation],
        }
    },
}
</script>