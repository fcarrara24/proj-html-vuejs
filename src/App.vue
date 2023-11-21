<template>
  <div>
    <TimerComponent />
    <HeaderComponent />
    <HeroComponent />
    <BoxComponent />
  </div>
</template>

<script>
import BoxComponent from './components/BoxComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import TimerComponent from './components/TimerComponent.vue';

export default {
  name: "App",
  data() {
    return {};
  },
  components: { TimerComponent, HeaderComponent, HeroComponent, BoxComponent }
}
</script>

<style lang="scss" scoped></style>