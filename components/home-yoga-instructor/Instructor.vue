<template>
  <div class="edu-team-area team-area-4">
    <div class="container">
      <SectionTitle
        preTitle="Services"
        preTitleClass="pre-textsecondary"
        title="Empire Surveillance Service"
        alignment="section-center"
      />

      <div class="row g-5">
        <div
          class="col-lg-4 col-sm-6 col-12"
          data-aos-delay="150"
          data-aos="fade-up"
          data-aos-duration="800"
          v-for="(instructor, key) in yogaInstructors.slice(0, 3)"
          :key="key"
        >
          <InstructorFour :instructor="instructor" />
        </div>
      </div>
    </div>
    <ul class="shape-group">
      <MouseMove
        addClassName="shape-1"
        dataDepth="1"
        data-aos-delay="500"
        data-aos="fade"
        data-aos-duration="200"
        imgSrc="/images/others/shape-14.png"
      />
      <MouseMove
        addClassName="shape-2"
        dataDepth="-2"
        data-aos-delay="500"
        data-aos="fade"
        data-aos-duration="200"
        imgSrc="/images/others/shape-13.png"
      />
      <MouseMove
        addClassName="shape-3"
        dataDepth="2"
        data-aos-delay="500"
        data-aos="fade"
        data-aos-duration="200"
        imgSrc="/images/others/shape-12.png"
      />
    </ul>
  </div>
</template>

<script>
import instructorProfilesMixin from "~~/mixins/instructorProfilesMixin";
import MouseMove from "../animation/MouseMove.vue";
import InstructorFour from "../instructor/InstructorFour.vue";
import SectionTitle from "../common/SectionTitle.vue";
export default {
  mixins: [instructorProfilesMixin],
  components: {
    MouseMove,
    InstructorFour,
    SectionTitle,
  },
};
</script>
