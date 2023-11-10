<template>
    <div id="main-wrapper" class="main-wrapper">
        <YogaInstructorMain />
    </div>
</template>
<script>
import YogaInstructorMain from "~~/components/home-yoga-instructor/YogaInstructorMain.vue";

export default {
    name: "home",
    components: {
        YogaInstructorMain
    },
    created() {
        api().get("site-setting-show").then((res) => {
        if (res.data.success) {
          this.site = res.data.data;
        }
      });
        // $fetch('https://jsonplaceholder.typicode.com/users')
    }
};
</script>
<style scoped></style>