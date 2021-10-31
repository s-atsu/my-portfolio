<template>
  <footer class="l-footer">
    <div class="l-footer__inner">
      <div class="l-footer__main">
        <div class="l-footer__sns">
          <h2>s-atsu</h2>
        </div>
        <SiteNav layoutClass="c-siteNav--footer" />
      </div>
      <p class="l-footer__copyright">© s-atsu.</p>
    </div>
  </footer>
</template>

<style lang="scss">
.l-footer {
  height: 100vh;
  color: #1a1a1a;
  background: #fff;
  padding: 40px 0;

  a,
  a:visited {
    color: #1a1a1a;
  }
}
.l-footer__inner {
  max-width: 1140px;
  margin: 0 auto;
  padding: 0 40px;
}
.l-footer__main {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.l-footer__sns {
  width: 500px;
}
.c-siteNav--footer {
  .c-siteNav__inner {
    padding: 0;
    margin: 0;
    list-style: none;
    width: 500px;
    text-align: left;
    height: 200px;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
  }
  .c-siteNav__item {
    margin-bottom: 30px;
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
