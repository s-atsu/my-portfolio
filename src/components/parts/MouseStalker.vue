<template>
  <div class="c-mouseStalker">
    <span></span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mouseStalker: null,
      stalker: {
        x: 0,
        y: 0,
      },
      mouse: {
        x: 0,
        y: 0,
      },
    };
  },
  mounted() {
    document.addEventListener("DOMContentLoaded", this.init());
  },
  methods: {
    init: function () {
      this.mouseStalker = document.querySelector(".c-mouseStalker");

      this.stalkerUpdate();
    },
    stalkerUpdate: function () {
      this.stalker.x += (this.mouse.x - this.stalker.x) * 0.1;
      this.stalker.y += (this.mouse.y - this.stalker.y) * 0.1;

      let x = Math.round(this.stalker.x * 10) / 10;
      let y = Math.round(this.stalker.y * 10) / 10;

      this.mouseStalker.style.transform =
        `translate3d(` + x + "px," + y + "px, 0)";

      requestAnimationFrame(this.stalkerUpdate);
    },
    getMousePosition: function (e) {
      this.mouse.x = e.clientX;
      this.mouse.y = e.clientY;
    },
  },
};
</script>

<style lang="scss">
.c-mouseStalker {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 1px;
  height: 1px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9999;
  pointer-events: none;
  mix-blend-mode: exclusion;

  > span {
    width: 50px;
    height: 50px;
    border: 1px solid #fff;
    border-radius: 50%;
    flex-shrink: 0;
  }
}
</style>
