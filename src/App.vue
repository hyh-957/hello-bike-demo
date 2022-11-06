<template>

  <Menu></Menu>

  <Footer></Footer>




</template>

<style lang="less">

</style>

<script lang="ts" setup>
import Menu from "./components/Menu.vue";
import Footer from "./components/Footer.vue";

let oldVal = 0;
let newVal = 0;
window.addEventListener('scroll', (e) => {
  oldVal = newVal;
  newVal = document.documentElement.scrollTop;
  const dom = document.getElementsByClassName('header')[0] as HTMLElement;
  if (oldVal < newVal) { // 上滑
    dom.style.transform = 'translate(0, -150%)';
  } else { // 下滑
    dom.style.transform = 'translate(0, 0)';
  }

  if (document.documentElement.scrollTop > 0) {
    dom.style.backgroundColor = '0096ff';
    dom.style.opacity = '0.8';
  } else {
    dom.style.backgroundColor = 'transparent';
  }
})
</script>
