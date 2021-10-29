<template>
  <header class="l-header">
    <div class="l-header__content">
      <div class="l-header__logo">
        <h1>s-atsu</h1>
      </div>
      <nav class="l-header__nav">
        <ul>
          <li class="l-header__item">
            <router-link to="/">SERVICE</router-link>
          </li>
          <li class="l-header__item">
            <router-link to="/">ABOUT</router-link>
          </li>
          <li class="l-header__item">
            <router-link to="/">WORKS</router-link>
          </li>
          <li class="l-header__item">
            <router-link to="/">INFOMATION</router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
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
.l-header__nav {
  ul {
    list-style: none;
    display: flex;
    padding: 0;
    margin: 0;
  }
}
.l-header__item {
  & + .l-header__item {
    margin-left: 15px;
  }
}
</style>
