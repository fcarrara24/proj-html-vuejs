<template>
  <div>
    <TimerComponent />
    <HeaderComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import TimerComponent from './components/TimerComponent.vue';

export default {
  name: "App",
  data() {
    return {};
  },
  components: { TimerComponent, HeaderComponent }
}
</script>

<style lang="scss" scoped></style>