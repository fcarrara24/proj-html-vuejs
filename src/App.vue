<template>
  <div>
    <HeaderComponent />

    <HeroComponent />
    <BoxComponent />
    <TestimonialsComponent />
    <CourseComponent />
    <BlogComponent />
    <EventComponent />
    <GetContactComponent />
    <FooterComponent />
  </div>
</template>

<script>
import BlogComponent from './components/BlogComponent.vue';
import BoxComponent from './components/BoxComponent.vue';
import CourseComponent from './components/CourseComponent.vue';
import EventComponent from './components/EventComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import GetContactComponent from './components/GetContactComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import TestimonialsComponent from './components/TestimonialsComponent.vue';



export default {
  name: "App",
  data() {
    return {};
  },
  components: { HeaderComponent, HeroComponent, BoxComponent, TestimonialsComponent, CourseComponent, BlogComponent, EventComponent, GetContactComponent, FooterComponent }
}
</script>

<style lang="scss" scoped>
@use './assets/style/main' as *;
@use './assets/style/partials/variables' as *;
</style>