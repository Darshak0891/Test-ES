<template>
  <div class="edu-instagram-area instagram-area-1">
    <div class="container-fluid">
      <SectionTitle
        preTitleClass="pre-textsecondary"
        title="Our Team"
        alignment="section-center"
      />

      <div class="row g-3">
        <div
          class="col-xl-2 col-md-4 col-sm-6"
          v-for="(instagram, index) in yogaPosts"
          :key="index"
        >
          <InstagramPost :instagram="instagram" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import instagramMixin from "~~/mixins/instagramMixin";
import InstagramPost from "../InstagramPost.vue";
import SectionTitle from "../common/SectionTitle.vue";

export default {
  mixins: [instagramMixin],
  components: {
    InstagramPost,
    SectionTitle,
  },
};
</script>
