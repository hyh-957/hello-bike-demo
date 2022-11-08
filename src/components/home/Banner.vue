<template>
  <section class="top__banner">
    <video id="video-player" src="../../../public/static/video/home_bg_video_v3.mp4" autoplay loop
      poster="../../../public/static/image/home_bg_video_v3.jpg"></video>
    <div class="banner__body">
      <div class="slogan">
        <span class="line line-1">哈啰</span>
        <span class="line line-2">陪伴生活每一天</span>
      </div>
      <div class="operation">
        <div class="operation--button download">
          <img src="../../../public/static/image/index__download.png" alt="下载">
          <span>下载客户端</span>
          <div class="operation__qr">
            <div class="operation__qr--body">
              <img src="../../../public/static/image/index__download.png" alt="">
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
  width: 992px;
  z-index: 3;
}

.slogan {
  display: flex;
  flex-direction: column;
  color: #fff;
  font-size: 48px;
  font-weight: 500;
}

.operation {
  display: inline-flex;
  margin-top: 48px;
}

.operation--button {
  position: relative;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 128px;
  height: 32px;
  background: rgba(0, 0, 0, .2);
  border-radius: 3px;
  border: 1px solid #fff;
  color: #fff;
  text-align: center;
  line-height: 16px;
  font-size: 16px;
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
    top: 48px;
  }
}



.operation--button>img {
  width: 16px;
  height: 16px;
  margin-right: 10px;
}

.operation__qr {
  position: absolute;
  transition: all .3s ease;
  transform-origin: 50% 0 0;
  width: 128px;
  height: 128px;
  box-sizing: border-box;
  background: #fff;
  top: 4px;
  padding: 4px;
  opacity: 0;
  cursor: initial;
  border-radius: 4px;
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
    top: -16px;
    width: 0;
    height: 0;
    border: 8px solid transparent;
    border-bottom: 8px solid #fff;
    margin-left: -8px;
  }
}

@media screen and (max-width: 992px) {
  .banner__body {
    width: 100%;
  }
}
</style>
