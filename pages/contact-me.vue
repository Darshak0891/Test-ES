<template>
  <div id="main-wrapper" class="main-wrapper">
    <HeaderOne />

    <BreadCrumbTwo title="Career" />

    <section class="section-gap-equal contact-me-area">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-xl-9">
            <div class="contact-me">
              <div class="inner">
                <div class="thumbnail">
                  <div class="thumb">
                    <img src="/images/others/contact-me.jpg" alt="Contact Me" />
                  </div>
                  <ul class="shape-group">
                    <MouseMove
                      addClassName="shape-1"
                      dataDepth="1.4"
                      imgSrc="/images/about/shape-13.png"
                    />
                    <MouseMove
                      addClassName="shape-2"
                      dataDepth="-1.4"
                      imgSrc="/images/counterup/shape-02.png"
                    />
                    <li class="shape-3">
                      <img src="/images/about/shape-07.png" alt="Shape" />
                    </li>
                  </ul>
                </div>

                <div class="contact-us-info">
                  <!-- <h3 class="heading-title">
                    I will Answer all Your Questions
                  </h3> -->
                  <ul class="address-list">
                    <li>
                      <h5 class="title">Designation</h5>
                      <p>Web Developer</p>
                    </li>
                    <li>
                      <h5 class="title">Description</h5>
                      <p>This is the description.</p>
                    </li>
                    <li>
                      <h5 class="title">year Of Experience</h5>
                      <p>
                        <a href="tel:+0914135548598">5</a>
                      </p>
                    </li>
                    <li>
                      <h5 class="title">Total Position</h5>
                      <p>
                        <a href="tel:+0914135548598">20</a>
                      </p>
                    </li>
                  </ul>

                  <ul class="social-share">
                    <li>
                      <a href="#"><i class="icon-share-alt"></i></a>
                    </li>
                    <li>
                      <a href="#"><i class="icon-facebook"></i></a>
                    </li>
                    <li>
                      <a href="#"><i class="icon-twitter"></i></a>
                    </li>
                    <li>
                      <a href="#"><i class="icon-linkedin2"></i></a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="edu-section-gap contact-form-area">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8">
            <div class="contact-form">
              <div class="section-title section-center">
                <h3 class="title">Just Drop Me a Line</h3>
              </div>

              <form
                class="rnt-contact-form rwt-dynamic-form"
                ref="form"
                @submit.prevent="sendEmail"
              >
                <div class="row row--10">
                  <div class="form-group col-lg-6">
                    <input
                      type="text"
                      name="fullname"
                      placeholder="Your Name"
                    />
                  </div>
                  <div class="form-group col-lg-6">
                    <input type="email" name="email" placeholder="Your Email" />
                  </div>
                  <div class="form-group col-12">
                    <input type="tel" name="phone" placeholder="Phone number" />
                  </div>
                  <div class="form-group col-12">
                    <textarea
                      name="message"
                      cols="30"
                      rows="6"
                      placeholder="Type your message"
                    ></textarea>
                  </div>
                  <div class="form-group col-12 text-center">
                    <button
                      class="rn-btn edu-btn submit-btn"
                      name="submit"
                      type="submit"
                    >
                      Submit Now <i class="icon-4"></i>
                    </button>
                    <div v-if="showResult" class="col-12 success-msg">
                      <p>{{ resultText }}</p>
                    </div>
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
      <ul class="shape-group">
        <MouseMove
          addClassName="shape-1"
          dataDepth="-2"
          imgSrc="/images/about/shape-15.png"
        />
        <MouseMove
          addClassName="shape-2"
          dataDepth="2"
          imgSrc="/images/cta/shape-04.png"
        />
        <MouseMove addClassName="shape-3" dataDepth="1" />
        <MouseMove
          addClassName="shape-4"
          dataDepth="-2"
          imgSrc="/images/about/shape-13.png"
        />
      </ul>
    </section>

    <FooterOne />
    <ScrollToTop />
  </div>
</template>

<script>
import emailjs from "emailjs-com";
import MouseMove from "~~/components/animation/MouseMove.vue";
import BreadCrumbTwo from "~~/components/common/BreadCrumbTwo.vue";
import HeaderOne from "~~/components/header/HeaderOne.vue";
import ScrollToTop from "~~/components/footer/ScrollToTop.vue";

export default {
  components: {
    MouseMove,
    HeaderOne,
    BreadCrumbTwo,
    ScrollToTop,
  },
  data() {
    return {
      resultText: "",
      showResult: false,
    };
  },
  methods: {
    sendEmail(e) {
      emailjs
        .sendForm(
          "service_bxh6md3",
          "template_1g7v07n",
          this.$refs.form,
          "user_8Lx0gfI1ktOoeEN8DTV10"
        )
        .then(
          (result) => {
            this.showResult = true;
            this.resultText =
              "Your message has been sent successfully. We will contact you soon.";
            setTimeout(() => {
              this.showResult = false;
            }, 5000);
            e.target.reset();
            console.log("SUCCESS!", result.text);
          },
          (error) => {
            this.showResult = true;
            this.resultText = error.text;
            setTimeout(() => {
              this.showResult = false;
            }, 5000);
            console.log("FAILED...", error.text);
          }
        );
    },
  },
  head() {
    return {
      title: "Contact Me",
    };
  },
};
</script>
