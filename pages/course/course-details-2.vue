<template>
  <div id="main-wrapper" class="main-wrapper">
    <HeaderOne />

    <div class="edu-breadcrumb-area breadcrumb-style-3">
      <div class="container">
        <div class="breadcrumb-inner">
          <ul class="edu-breadcrumb">
            <li class="breadcrumb-item">
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li class="separator"><i class="icon-angle-right"></i></li>
            <li class="breadcrumb-item">
              <NuxtLink to="/course/course-one">Case Study</NuxtLink>
            </li>
            <li class="separator"><i class="icon-angle-right"></i></li>
            <li class="breadcrumb-item active" aria-current="page">
              Case Study Details
            </li>
          </ul>
          <div class="page-title">
            <h1 class="title">Global Education Fall Meeting for Everyone</h1>
          </div>
          <ul class="course-meta">
            <li><i class="icon-58"></i>by Edward Norton</li>
            <li><i class="icon-59"></i>English</li>
            <li class="course-rating">
              <div class="rating">
                <i class="icon-23"></i>
                <i class="icon-23"></i>
                <i class="icon-23"></i>
                <i class="icon-23"></i>
                <i class="icon-23"></i>
              </div>
              <span class="rating-count">(720 Rating)</span>
            </li>
          </ul>
        </div>
      </div>
      <ul class="shape-group">
        <li class="shape-1">
          <span></span>
        </li>
        <MouseMove
          addClassName="shape-2"
          dataDepth="2"
          imgSrc="/images/about/shape-13.png"
        />
        <MouseMove
          addClassName="shape-3"
          dataDepth="-2"
          imgSrc="/images/about/shape-15.png"
        />
        <li class="shape-4">
          <span></span>
        </li>
        <li class="shape-5">
          <img src="/images/about/shape-07.png" alt="shape" />
        </li>
      </ul>
    </div>

    <section class="edu-section-gap course-details-area">
      <div class="container">
        <div class="row row--30">
          <div class="col-lg-8">
            <div class="course-details-content course-details-2">
              <div class="course-overview">
                <h3
                  class="heading-title"
                  data-aos-delay="150"
                  data-aos="fade-up"
                  data-aos-duration="800"
                >
                  About This Case Study
                </h3>
                <p
                  data-aos-delay="150"
                  data-aos="fade-up"
                  data-aos-duration="800"
                >
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor inc idid unt ut labore et dolore magna
                  aliqua enim ad minim veniam, quis nostrud exerec tation
                  ullamco laboris nis aliquip commodo consequat duis aute irure
                  dolor in reprehenderit in voluptate velit esse cillum dolore
                  eu fugiat nulla pariatur enim ipsam.
                </p>
                <p
                  data-aos-delay="150"
                  data-aos="fade-up"
                  data-aos-duration="800"
                >
                  Excepteur sint occaecat cupidatat non proident sunt in culpa
                  qui officia deserunt mollit anim id est laborum. Sed ut
                  perspiciatis unde omnis iste natus error sit voluptatem
                  accusantium doloremque laudantium totam rem aperiam.
                </p>
                <div class="border-box">
                  <h5
                    class="title"
                    data-aos-delay="150"
                    data-aos="fade-up"
                    data-aos-duration="800"
                  >
                    What You’ll Learn?
                  </h5>
                  <div class="row g-5">
                    <div
                      class="col-lg-6"
                      data-aos-delay="150"
                      data-aos="fade-up"
                      data-aos-duration="800"
                    >
                      <ul>
                        <li>
                          Learn to use Python professionally, learning both
                          Python 2 & Python 3!
                        </li>
                        <li>
                          Build 6 beautiful real-world projects for your
                          portfolio (not boring toy apps)
                        </li>
                      </ul>
                    </div>
                    <div
                      class="col-lg-6"
                      data-aos-delay="150"
                      data-aos="fade-up"
                      data-aos-duration="800"
                    >
                      <ul>
                        <li>
                          Understand the Theory behind Vue.js and use it in Real
                          Projects
                        </li>
                        <li>
                          Create responsive, accessible, and beautiful layouts
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="course-sidebar-3">
              <div class="edu-course-widget widget-course-summery">
                <div class="inner">
                  <div class="thumbnail"></div>
                  <div class="content">
                    <h4 class="widget-title">Case Study:</h4>
                    <ul class="course-item">
                      <li>
                        <span class="label"
                          ><i class="icon-62"></i>Instrutor:</span
                        >
                        <span class="value">Edward Norton</span>
                      </li>
                      <li>
                        <span class="label"
                          ><i class="icon-61"></i>Duration:</span
                        >
                        <span class="value">3 weeks</span>
                      </li>
                      <li>
                        <span class="label">
                          <CourseDetailsOne />
                          Lessons:
                        </span>
                        <span class="value">8</span>
                      </li>
                      <li>
                        <span class="label"
                          ><i class="icon-63"></i>Enrolled:</span
                        >
                        <span class="value">65 students</span>
                      </li>
                      <li>
                        <span class="label"
                          ><i class="icon-59"></i>Language:</span
                        >
                        <span class="value">English</span>
                      </li>
                      <li>
                        <span class="label"
                          ><i class="icon-64"></i>Certificate:</span
                        >
                        <span class="value">Yes</span>
                      </li>
                    </ul>
                    <div class="share-area">
                      <h4 class="title">Share On:</h4>
                      <ul class="social-share">
                        <li>
                          <a href="#"><i class="icon-facebook"></i></a>
                        </li>
                        <li>
                          <a href="#"><i class="icon-twitter"></i></a>
                        </li>
                        <li>
                          <a href="#"><i class="icon-linkedin2"></i></a>
                        </li>
                        <li>
                          <a href="#"><i class="icon-youtube"></i></a>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <FooterOne />
    <ScrollToTop />

    <!-- video modal start -->
    <video-modal
      ref="video_modal"
      video-url="https://www.youtube.com/embed/7e90gBu4pas"
    />
    <!-- video modal end -->
  </div>
</template>

<script>
import HeaderOne from "~~/components/header/HeaderOne.vue";
import FooterOne from "~~/components/footer/FooterOne.vue";
import MouseMove from "~~/components/animation/MouseMove.vue";
import ScrollToTop from "~~/components/footer/ScrollToTop.vue";

import VideoModal from "../../components/common/VideoModal.vue";
import CourseDetailsOne from "~~/components/svg/CourseDetailsOne.vue";

export default {
  components: {
    HeaderOne,
    FooterOne,
    MouseMove,
    VideoModal,
    CourseDetailsOne,
    ScrollToTop,
  },
  head() {
    return {
      title: "Course Details 2",
    };
  },
  methods: {
    handleVideoPopup() {
      this.$refs.video_modal.playVideo();
    },
  },
};
</script>
