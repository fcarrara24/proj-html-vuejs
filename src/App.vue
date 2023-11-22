<template>
  <div>
    <TimerComponent />
    <HeaderComponent />
    <HeroComponent />
    <BoxComponent />
    <TestimonialsComponent />
    <CourseComponent />
    <BlogComponent />
    <EventComponent />
  </div>
</template>

<script>
import BlogComponent from './components/BlogComponent.vue';
import BoxComponent from './components/BoxComponent.vue';
import CourseComponent from './components/CourseComponent.vue';
import EventComponent from './components/EventComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import TestimonialsComponent from './components/TestimonialsComponent.vue';
import TimerComponent from './components/TimerComponent.vue';


export default {
  name: "App",
  data() {
    return {};
  },
  components: { TimerComponent, HeaderComponent, HeroComponent, BoxComponent, TestimonialsComponent, CourseComponent, BlogComponent, EventComponent }
}
</script>

<style lang="scss" scoped>
@use './assets/style/main' as *;
@use './assets/style/partials/variables' as *;
</style>