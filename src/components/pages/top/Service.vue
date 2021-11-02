<template>
  <section class="p-index__service l-section">
    <div class="l-container">
      <h2 class="p-index__title">
        SERVICE
        <span class="p-index__subtitle">サービス</span>
      </h2>

      <ul class="p-index__services">
        <li
          class="p-index__services-item"
          v-for="service in services"
          :key="service.title"
        >
          <div class="p-index__services-text">
            <h3 class="p-index__title">
              {{ service.title }}
              <span class="p-index__subtitle">
                {{ service.subtitle }}
              </span>
            </h3>
            <p class="p-index__text" v-html="service.description"></p>
          </div>
          <div class="p-index__services-img">
            <img :src="service.img" />
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
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
.p-index__title {
  font-size: 30px;
  font-weight: bold;
}
.p-index__subtitle {
  font-size: 14px;
  display: block;
}
.p-index__services {
  list-style: none;
  padding: 0;
  margin-top: 50px;
  margin-bottom: 0;
}
.p-index__services-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.p-index__services-text {
  width: 48%;
  text-align: left;
}
.p-index__text {
  font-size: 20px;
  line-height: 1.7;
}
.p-index__services-img {
  width: 48%;
  max-width: 500px;
}
</style>

<script>
export default {
  data() {
    return {
      // サービス一覧を定義
      services: [
        {
          title: "WEB PRODUCTION",
          subtitle: "WEB製作",
          description:
            "コーポレートサイト・ブランドサイト等<br />様々なWebサイト制作に対応可能です。<br />アニメーションを活用したサイト制作も承っております。<br />ご気軽にご相談ください。",
          img: require("../../../assets/images/webproduct.jpg"),
        },
      ],
    };
  },
};
</script>
