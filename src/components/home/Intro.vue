

<template>
  <section class="intro">
    <div class="container">
      <div class="video" data-src="https://www.hello-inc.com/online-public/2022-hello-brand.mp4">
      <img class="preview-image" src="../../../public/static/image/index-intro-preview.png" alt="play">
      <img class="play-icon" src="../../../public/static/image/index-play-icon.png" alt="">
    </div>
    <div class="text">
      <header>
        哈啰
      </header>
      <main>
        国内专业的本地出行及生活服务平台，致力于应用数字技术的红利，为人们提供更便捷的出行以及更好的普惠生活服务。公司成立于2016年9月，总部位于上海，从大家熟悉的共享单车业务起步。目前哈啰主要提供移动出行服务及新兴本地服务。
      </main>
    </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref } from "vue";


</script>

<style lang="less" scoped>

.intro{
  width: 100%;
  padding: 80px 0;
  background: #f5f8fb;
}

.intro > .container{
  display: flex;
  justify-content: center;
}

.container>.video,
.container>.text {
  width: 500px;
}

.video {
  position: relative;
}

.text {
  margin-left: 40px;
}

header {
  font-size: 28px;
  margin-bottom: 16px;
}

main {
  font-size: 16px;
  letter-spacing: 1px;
  padding-right: 16px;
  line-height: 1.5;
}

.preview-image {
  height: 300px;
  width: 500px;
}

.play-icon {
  height: 108px;
  width: 108px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  cursor: pointer;
}
</style>