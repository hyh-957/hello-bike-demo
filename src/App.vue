<template>
  <div class="app-container">
  <Menu></Menu>
  <Footer></Footer>
</div>

</template>

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
    dom.style.backgroundColor = '#0096ff';
    dom.style.opacity = '0.8';
  } else {
    dom.style.backgroundColor = 'transparent';
  }
})
</script>

<style lang="less">
@media screen and (max-width: 768px) {
  .test {
    color: aliceblue;
  }
}

@media screen and (min-width:768px) and (max-width: 992px) {
  .test {
    color: black;
  }
}

@media screen and (min-width:992px) and (max-width: 1200px) {
  .test {
    color: blue;
  }
}

@media screen and (min-width:1200px) and (max-width: 1920px) {
  .test {
    color: white;
  }
}

.app-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
