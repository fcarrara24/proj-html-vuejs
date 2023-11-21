<template>
  <div>
    <TimerComponent />
    <HeaderComponent />
    <HeroComponent />
    <BoxComponent />
    <TestimonialsComponent />
    <CourseComponent />
  </div>
</template>

<script>
import BoxComponent from './components/BoxComponent.vue';
import CourseComponent from './components/CourseComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import TestimonialsComponent from './components/TestimonialsComponent.vue';
import TimerComponent from './components/TimerComponent.vue';

export default {
  name: "App",
  data() {
    return {};
  },
  components: { TimerComponent, HeaderComponent, HeroComponent, BoxComponent, TestimonialsComponent, CourseComponent }
}
</script>

<style lang="scss" scoped></style>