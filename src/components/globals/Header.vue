<template>
  <header class="l-header">
    <div class="l-header__content">
      <div class="l-header__logo">
        <h1>s-atsu</h1>
      </div>
      <SiteNav layoutClass="c-siteNav--header" />
    </div>
  </header>
</template>

<style lang="scss">
.l-header {
  padding: 50px;
}
.l-header__content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.l-header__logo {
  h1 {
    margin: 0;
  }
}
.c-siteNav--header {
  .c-siteNav__inner {
    list-style: none;
    display: flex;
    padding: 0;
    margin: 0;
  }
  .c-siteNav__item {
    & + .c-siteNav__item {
      margin-left: 15px;
    }
  }
}
</style>

<script>
import SiteNav from "../parts/SiteNav.vue";

export default {
  components: {
    SiteNav,
  },
};
</script>
