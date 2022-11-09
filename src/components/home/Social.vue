
<template>
  <section class="social">
    <div class="container">
      <div class="top">
        <div class="title">
          <div class="line-1">社会责任</div>
          <div class="line-2">Social Responsibility</div>
        </div>
        <button class="more">了解更多</button>

      </div>

      <div class="duty-statistics">
        <div class="duty-statistics-left">
          <div class="duty-item">
            <div class="duty-item-top">
              <div class="duty-item-number">416</div>
              <div class="duty-item-sub">亿公里</div>
            </div>
            <div class="duty-item-desc">骑行总里程</div>
          </div>
          <div class="duty-item">
            <div class="duty-item-top">
              <div class="duty-item-number">104</div>
              <div class="duty-item-sub">万圈</div>
            </div>
            <div class="duty-item-desc">绕地球圈数</div>
          </div>
          <div class="duty-item">
            <div class="duty-item-top">
              <div class="duty-item-number">194</div>
              <div class="duty-item-sub">万吨</div>
            </div>
            <div class="duty-item-desc">碳排放减少量</div>
          </div>
        </div>
        <div class="duty-statistics-right"><img class="duty-earth"
            src="https://www.hello-inc.com/online-public/index/index__earth.gif" alt="地球">
          <div class="duty-statistics-right-title">共享出行为地球减负</div>
        </div>
      </div>
    </div>



  </section>
</template>

<script lang="ts" setup>

</script>


<style scoped lang="less">
.social {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
}

.container {
  width: 950px;
  padding: 95px 0;
}

.top {
  display: flex;
  justify-content: space-between;
}

.title {
  margin-bottom: 74px;
}

.line-1 {
  font-size: 30px;
  height: 44px;
}

.line-2 {
  font-size: 18px;
  height: 26px;
}

.more {
  height: 36px;
  width: 90px;
  border: 1px solid #e5e5e5;
  font-size: 12px;
  color: #999;
  cursor: pointer;

  &:hover {
    background: #0096ff;
    border-color: #0096ff;
    opacity: 1;
    color: #fff;
  }
}

.duty-statistics {
  display: flex;
  justify-content: space-between;
}

.duty-statistics-left {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.duty-item {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.duty-item-top {
  display: flex;
  align-items: baseline;
}

.duty-item-number {
  font-size: 70px;
  font-weight: 700;
  color: #0096ff;
  margin-right: 8px;
}

.duty-item-sub {
  font-size: 20px;
  font-weight: 500;
  color: #333;
}

.duty-item-desc {
  font-size: 16px;
  font-weight: 300;
  color: #999;
  margin-top: 10px;
}

.duty-statistics-right-title {
  text-align: center;
  font-weight: 400;
  color: #0096ff;
}

@media screen and (max-width: 992px) {
  .duty-item-top {
    flex-direction: column;
    align-items: center;
  }

  .duty-item-desc{
    text-align: center;
  }
}
</style>
