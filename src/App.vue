<template>
  <div class="l-page" v-on:mousemove="callChildMethod()">
    <Loading v-show="loading" />
    <MouseStalker ref="child" />

    <Header />

    <router-view></router-view>

    <Footer />
  </div>
</template>

<style lang="scss">
body {
  font-family: "游ゴシック体", YuGothic, "游ゴシック Medium", "Yu Gothic Medium",
    "游ゴシック", "Yu Gothic", "ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro",
    "メイリオ", Meiryo, Osaka, "ＭＳ Ｐゴシック", "MS PGothic", sans-serif;
  background: #1a1a1a;
  color: #f1f1f1;
  text-align: center;
}
a {
  &:link,
  &:visited {
    color: #f1f1f1;
    text-decoration: none;
  }
}
img {
  width: 100%;
}
.l-section {
  padding: 0 40px;
  margin-top: 100px;
}
.l-container {
  max-width: 1140px;
  margin: 0 auto;
  padding: 40px;
  border-top: 1px solid #fff;
}
</style>

<script>
import "normalize.css";
import Loading from "./components/parts/Loading.vue";
import MouseStalker from "./components/parts/MouseStalker.vue";
import Header from "./components/globals/Header.vue";
import Footer from "./components/globals/Footer.vue";

export default {
  name: "App",
  data() {
    return {
      loading: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 2600);
  },
  components: {
    Loading,
    MouseStalker,
    Header,
    Footer,
  },
  methods: {
    callChildMethod() {
      this.$refs.child.getMousePosition(event);
    },
  },
};
</script>
