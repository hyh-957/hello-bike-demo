<template>
  <section class="technology">
    <el-carousel trigger="click" :autoplay=false arrow="always">
      <el-carousel-item v-for="item in 4" :key="item">
        <div class="slide-item">
          <div class="tech-body">
            <div class="tech-body-title">普惠</div>
            <div class="tech-body-desc">坚持以用户为中心，</div>
            <div class="tech-body-desc">提供更多可负担的选择。</div>
          </div>
        </div>
      </el-carousel-item>
    </el-carousel>
  </section>

</template>

<script lang="ts" setup>

</script>


<style scoped lang="less">
.technology {
  height: 100vh;
  width: 100;
  width: 100%;
}

/deep/.el-carousel__container {
  height: 100vh;
}

.slide-item {
  background-image: url(../../../public/static/image/index-tech-slide-0.png);
  background-size: 100% 100%;
  height: 100%;
  width: 100%;
  position: relative;
}

.tech-body{
  color: #fff;
  position: absolute;
  top: 80px;
  left: 280px;
}

.tech-body-title{
  font-size: 44px;
  font-weight: 500;
  margin-bottom: 20px;
}

.tech-body-desc{
  font-size: 25px;
}
</style>