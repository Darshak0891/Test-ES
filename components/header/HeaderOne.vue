<template>
  <header class="edu-header header-style-1 header-fullwidth no-topbar">
    <HeaderTopOne v-if="showHeaderTop" />
    <div class="header-mainmenu" :class="{ 'edu-sticky': isSticky }">
      <div class="container-fluid">
        <div class="header-navbar">
          <div class="header-brand">
            <div class="logo">
              <NuxtLink to="/">
                <img
                  class="logo-light"
                  src="/images/logo/logo-dark.png"
                  alt="Dark Logo"
                />
                <img
                  class="logo-dark"
                  src="/images/logo/logo-white.png"
                  alt="Light Logo"
                />
              </NuxtLink>
            </div>
          </div>
          <div class="header-mainnav">
            <nav class="mainmenu-nav">
              <Navigation />
            </nav>
          </div>
        </div>
      </div>
    </div>

    <SearchPopUp />

    <OffCanvasMobileMenuOne />
  </header>
</template>

<script>
import Navigation from "./Navigation.vue";
import HeaderTopOne from "./HeaderTopOne.vue";
import OffCanvasMobileMenuOne from "./OffCanvasMobileMenuOne.vue";
import SearchPopUp from "./SearchPopUp.vue";

export default {
  components: {
    Navigation,
    HeaderTopOne,
    OffCanvasMobileMenuOne,
    SearchPopUp,
  },
  data() {
    return {
      isSticky: false,
    };
  },
  props: ["showHeaderTop"],
  mounted() {
    window.addEventListener("scroll", () => {
      let scrollPos = window.scrollY;
      if (scrollPos >= 200) {
        this.isSticky = true;
      } else {
        this.isSticky = false;
      }
    });
  },
  methods: {
    // Off-canvas Mobile Menu Open
    mobileMenuOpen(addRemoveClass, className) {
      const el = document.querySelector("#offcanvas-menu");
      if (addRemoveClass === "addClass") {
        el.classList.add(className);
      } else {
        el.classList.remove(className);
      }
    },

    // search popup
    searchPopUpOpen(addRemoveClass, className) {
      const el = document.querySelector("#edu-search-popup");
      if (addRemoveClass === "addClass") {
        el.classList.add(className);
      } else {
        el.classList.remove(className);
      }
    },
  },
};
</script>
