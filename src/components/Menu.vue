<template>

    <header class="header">
      <div class="container">
        <div class="logo" @click="$router.push('/')">
          <img src="../../public/static/image/hs3_c_header__logo.png" alt="">
          <button>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
        </div>
      <el-menu :default-active="$route.path" class="el-menu-demo" mode="horizontal" :ellipsis="false"
        @select="handleSelect" :router="true">
        
        <!-- <div class="flex-grow"></div> -->
        <el-menu-item index="/" route>首页</el-menu-item>
        <el-menu-item index="/about">哈啰业务</el-menu-item>
        <el-menu-item index="/about">哈啰科技</el-menu-item>
        <el-menu-item index="/about">咨询中心</el-menu-item>
        <el-menu-item index="/about">关于我们</el-menu-item>
        <el-menu-item index="/about">联系我们</el-menu-item>
      </el-menu>
      </div>

    </header>
    <router-view />
 



</template>

<script lang="ts" setup>
import { ref } from "vue";

const activeIndex = ref("1");
const handleSelect = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>

<style lang="less" scoped>


.header {
  position: fixed;
  top: 0;
  z-index: 11;
  transition: all .6s cubic-bezier(.51,.01,0,1);
  background-color: aqua;
}

.container{
  display: flex;
  height: 80px;
  width: 992px;
  align-items: center;
  justify-content: space-between;
}

.el-menu-demo {
  // height: 80px;
  // width: 992px;
  background-color: transparent;
  align-items: center;
  justify-content: center;
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

.el-menu--horizontal>.el-menu-item.is-active {
  color: #fff !important;
  border-bottom: 2px solid #fff;
}

.el-menu--horizontal .el-menu-item:not(.is-disabled):focus {
  background-color: transparent;
}

.logo {
  height: 40px;
  width: 175px;

}

.icon-bar{
  background: #555;
    height: 2px;
    margin: 6px;
    width: 26px;
    display: block;
}

.flex-grow {
  flex-grow: 1;
}
</style>
