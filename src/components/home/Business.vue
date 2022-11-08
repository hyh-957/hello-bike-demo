<template>
  <section class="business">
    <div class="container">
      <div class="title">
        <div class="line-1">业务布局</div>
        <div class="line-2">Business Layout</div>
      </div>
      <div class="content">

        <el-carousel trigger="click" :autoplay=false arrow="always" indicator-position="outside">
          <el-carousel-item v-for="item in 3" :key="item" class="slide-container">
            <div class="slide-item">
              <img src="../../../public/static/image/index-slide-1-1.png" alt=""
                class="slide-item-img">
              <span class="slide-item-title">哈啰骑行</span>
              <span class="slide-item-desc">
                <span>科技引领两轮出行进化，持续迭代好骑的用户体验，智慧运营推动绿色低碳出行普及。</span>
              </span>
            </div>
            <div class="slide-item">
              <img src="../../../public/static/image/index-slide-1-1.png" alt=""
                class="slide-item-img">
              <span class="slide-item-title">哈啰骑行</span>
              <span class="slide-item-desc">
                <span>科技引领两轮出行进化，持续迭代好骑的用户体验，智慧运营推动绿色低碳出行普及。</span>
              </span>
            </div>
          </el-carousel-item>
        </el-carousel>

      </div>
    </div>

  </section>
</template>

<script lang="ts" setup>

</script>


<style scoped lang="less">
.business {
  height: 700px;
  width: 100%;
  padding: 80px 0;
}

.container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin: 0 auto;
  width: 992px;
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
/deep/.el-carousel__arrow  svg{
  color: black;
}

.slide-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.slide-item:first-child {
  margin-right: 150px;
}

.slide-item {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.slide-item-img {
  height: 134px;
  width: 134px;
}

.slide-item-title {
  font-size: 20px;
  font-weight: 500;
  margin: 20px 0;
}


.slide-item-desc {
  width: 160px;
  font-size: 12px;
  text-align: center;
}

/deep/.el-carousel__indicators--outside{
  border-bottom: 1px solid #e5e5e5;
}

/deep/ li.el-carousel__indicator.el-carousel__indicator--horizontal {
  width: 120px;
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0;
 

  &::before {
    content: '共享出行服务';
    font-size: 12px;
    color: #999;
    padding: 0 0 14px;
  }

  &.is-active::before {
    font-size: 16px;
    font-weight: 500;
    color: #0096ff;
  }

  &>.el-carousel__button {
    width: 80px;
    background-color: transparent
  }

  &.is-active>.el-carousel__button{
    background-color: #0096ff;;
  }
}

@media screen and (max-width: 992px) {
  .container {

  width: auto;
}
}
</style>