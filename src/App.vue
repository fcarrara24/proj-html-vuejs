<template>
  <div>
    <TimerComponent />
  </div>
</template>

<script>
import TimerComponent from './components/TimerComponent.vue';

export default {
  name: "App",
  data() {
    return {};
  },
  components: { TimerComponent }
}
</script>

<style lang="scss" scoped></style>