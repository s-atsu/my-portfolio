<template>
  <div class="shutter"></div>
</template>

<style scoped lang="scss">
.shutter {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #1a1a1a;
  z-index: 9999;
  animation: byeShutter 2.6s forwards;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    margin: auto;
    background-color: #f3f3f3;
    width: 0;
    height: 1px;
    animation: shutterOpen 2.6s forwards;
  }
}

@keyframes byeShutter {
  70% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    display: none;
    z-index: -1;
  }
}

@keyframes shutterOpen {
  0% {
    width: 0;
    height: 1px;
  }
  50% {
    width: 100%;
    height: 1px;
  }
  90% {
    width: 100%;
    height: 100%;
  }
  100% {
    width: 100%;
    height: 100%;
  }
}
</style>
