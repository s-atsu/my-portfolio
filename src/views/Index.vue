<template>
  <main class="p-index">
    <Mv />

    <Service />

    <About />
  </main>
</template>

<script>
import Mv from "../components/pages/top/Mv.vue";
import Service from "../components/pages/top/Service.vue";
import About from "../components/pages/top/About.vue";

export default {
  name: "Index",
  components: {
    Mv,
    Service,
    About,
  },
};
</script>

<style lang="scss">
.p-index__title {
  font-size: 30px;
  font-weight: bold;
}
.p-index__subtitle {
  font-size: 14px;
  display: block;
}
</style>
