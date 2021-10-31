<template>
  <nav class="c-siteNav" :class="layoutClass">
    <ul class="c-siteNav__inner">
      <li class="c-siteNav__item">
        <router-link to="/">TOP</router-link>
      </li>
      <li class="c-siteNav__item">
        <router-link to="/">SERVICE</router-link>
      </li>
      <li class="c-siteNav__item">
        <router-link to="/">ABOUT</router-link>
      </li>
      <li class="c-siteNav__item">
        <router-link to="/">WORKS</router-link>
      </li>
      <li class="c-siteNav__item">
        <router-link to="/">INFORMATION</router-link>
      </li>
      <li class="c-siteNav__item">
        <router-link to="/">CONTACT</router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: {
    layoutClass: {
      type: String,
      default: "",
      required: true,
    },
  },
};
</script>
