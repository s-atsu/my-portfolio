<template>
  <section class="p-index__mv">
    <ScrollDown />
  </section>
</template>

<style lang="scss" scoped>
.p-index__mv {
  height: 100vh;
}
</style>

<script>
import ScrollDown from "../../parts/ScrollDown.vue";

export default {
  components: {
    ScrollDown,
  },
};
</script>
