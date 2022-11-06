<template>
  <div class="app-container">
    <header class="header">
    <el-menu :default-active="$route.path" class="el-menu-demo" mode="horizontal" :ellipsis="false"
      @select="handleSelect" :router="true">
      <div class="logo" @click="$router.push('/')">
        <img src="../../public/static/image/hs3_c_header__logo.png" alt="">
      </div>
      <div class="flex-grow"></div>
      <el-menu-item index="/" route>首页</el-menu-item>
      <el-menu-item index="/about">哈啰业务</el-menu-item>
      <el-menu-item index="3">哈啰科技</el-menu-item>
      <el-menu-item index="4">咨询中心</el-menu-item>
      <el-menu-item index="5">关于我们</el-menu-item>
      <el-menu-item index="6">联系我们</el-menu-item>
    </el-menu>
  </header>
  <router-view />
  </div>



</template>

<script lang="ts" setup>
import { ref } from "vue";

const activeIndex = ref("1");
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>

<style lang="less" scoped>
.app-container{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.header {
  height: 80px;
  width: 100%;
  position: fixed;
  top: 0;
  padding: 0 276px;
  z-index: 11;
}

.el-menu-demo {
  height: 100%;
  background-color: transparent;
  align-items: center;
  border: 0;
  
  &>.el-menu-item {
    font-size: 16px;
    color: #fff;
    width: 104px;
  }

  &>.el-menu-item:hover {
    font-weight: 600;
    color: #fff;
    background-color: transparent;
    border-bottom: 2px solid #fff;
  }
}

.el-menu--horizontal>.el-menu-item.is-active{
  color: #fff !important;
  border-bottom: 2px solid #fff;
}

.el-menu--horizontal .el-menu-item:not(.is-disabled):focus{
  background-color: transparent;
}

.logo {
  height: 40px;
  width: 175px;

}

.flex-grow {
  flex-grow: 1;
}
</style>
