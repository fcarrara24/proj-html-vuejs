<template>
  <div>
    <TimerComponent />
    <HeaderComponent />
    <HeroComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import TimerComponent from './components/TimerComponent.vue';

export default {
  name: "App",
  data() {
    return {};
  },
  components: { TimerComponent, HeaderComponent, HeroComponent }
}
</script>

<style lang="scss" scoped></style>