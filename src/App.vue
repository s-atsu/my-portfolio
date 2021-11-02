<template>
  <div class="l-page">
    <Loading v-show="loading"></Loading>
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
</style>

<script>
import "normalize.css";
import Loading from "./components/parts/Loading.vue";
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
    Header,
    Footer,
  },
};
</script>
