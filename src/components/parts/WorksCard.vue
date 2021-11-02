<template>
  <div
    class="c-works__card"
    :style="{ backgroundImage: `url('${works.image}')` }"
  >
    <div class="c-works__content">
      <p class="c-works__title">{{ works.title }}</p>
      <p class="c-works__description">{{ works.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    works: [],
  },
};
</script>

<style lang="scss">
.c-works__card {
  width: calc(100% - 20px);
  background: #f5f5f5;
  background-size: 100%;
  padding-top: 100%;
}
</style>
