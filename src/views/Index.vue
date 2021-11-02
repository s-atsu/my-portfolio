<template>
  <main class="p-index">
    <Mv />

    <Service />
  </main>
</template>

<script>
import Mv from "../components/pages/top/Mv.vue";
import Service from "../components/pages/top/Service.vue";

export default {
  name: "Index",
  components: {
    Mv,
    Service,
  },
};
</script>
