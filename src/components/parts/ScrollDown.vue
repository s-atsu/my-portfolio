<template>
  <div class="c-scrollDown">SCROLL</div>
</template>

<style lang="scss" scoped>
.c-scrollDown {
  position: absolute;
  right: 40px;
  bottom: 0;
  z-index: 2;
  padding: 10px 10px 110px;
  overflow: hidden;
  color: #fff;
  font-size: 14px;
  font-family: "Josefin Sans", sans-serif;
  letter-spacing: 0.2em;
  writing-mode: vertical-lr;
}
.c-scrollDown::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 1px;
  height: 100px;
  background: rgba(255, 255, 255, 0.4);
}
.c-scrollDown::after {
  content: "";
  height: 30px;
  width: 1px;
  background: #fff;
  position: absolute;
  left: 50%;
  bottom: 0;
  animation: sdl 1.5s ease infinite;
}
@keyframes sdl {
  0% {
    transform: translateY(-70px);
  }
  50%,
  100% {
    transform: translateY(30px);
  }
}
</style>
