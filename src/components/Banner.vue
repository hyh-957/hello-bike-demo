<template>
  <section class="top__banner">
    <video id="video-player" src="../../public/static/video/home_bg_video_v3.mp4" autoplay loop
      poster="../../public/static/image/home_bg_video_v3.jpg"></video>
    <div class="banner__body">
      <div class="slogan">
        <span class="line line-1">哈啰</span>
        <span class="line line-2">陪伴生活每一天</span>
      </div>
      <div class="operation">
        <div class="operation--button download">
          <img src="../../public/static/image/index__download.png" alt="下载">
          <span>下载客户端</span>
          <div class="operation__qr">
            <div class="operation__qr--body">
              <img src="../../public/static/image/index__download.png" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>

</script>

<style lang="less" scoped>
.top__banner {
  width: 100%;
  min-width: 24rem;
  height: 100vh;
}

#video-player {
  height: 100%;
  width: 100%;
  object-fit: fill;
}

.banner__body {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 50rem;
  min-width: 24rem;
  z-index: 3;
}

.slogan {
  display: flex;
  flex-direction: column;
  color: #fff;
  font-size: 3rem;
  font-weight: 500;
}

.operation {
  display: inline-flex;
  margin-top: 3rem;
}

.operation--button {
  position: relative;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 8rem;
  height: 2rem;
  background: rgba(0, 0, 0, .2);
  border-radius: .02rem;
  border: .01rem solid #fff;
  color: #fff;
  text-align: center;
  line-height: 1rem;
  font-size: 1rem;
  cursor: pointer;
  opacity: .7;
  transition: all .3s ease;

  &:hover {
    background: #0096ff;
    border-color: #0096ff;
    opacity: 1;
  }

  &:hover>.operation__qr {
    visibility: visible;
    opacity: 1;
    top: 3rem;
  }
}



.operation--button>img {
  width: 1rem;
  height: 1rem;
  margin-right: .6rem;
}

.operation__qr {
  position: absolute;
  transition: all .3s ease;
  transform-origin: 50% 0 0;
  width: 8rem;
  height: 8rem;
  box-sizing: border-box;
  background: #fff;
  top: 3rem;
  padding: .2rem;
  opacity: 0;
  cursor: initial;
  border-radius: .2rem;
  pointer-events: none;
}

.operation__qr--body {
  height: 100%;
  width: 100%;
  background: #d8d8d8;

  &>img {
    height: 100%;
    width: 100%;
  }

  &::after {
    content: "";
    position: absolute;
    left: 50%;
    top: -1rem;
    width: 0;
    height: 0;
    border: .5rem solid transparent;
    border-bottom: .5rem solid #fff;
    margin-left: -0.5rem;
  }
}
</style>
