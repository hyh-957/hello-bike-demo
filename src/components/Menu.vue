<template>

  <header class="header">
    <div class="container" :class="{ 'c-container': isCollapse && isCollapse1 }">
      <div class="left-header">
        <div @click="$router.push('/')">
          <img class="logo" src="../../public/static/image/hs3_c_header__logo.png" alt="">
        </div>
        <button class="collapse-button" @click="collapse()">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
      </div>
      <div class="right-header" :class="{ 'c-right-header': isCollapse && isCollapse1 }">
        <el-menu :default-active="$route.path" class="el-menu-demo" mode="horizontal" :ellipsis="false" :router="true"
          :class="{ 'c-el-menu-demo': isCollapse && isCollapse1 }">
          <!-- <div class="flex-grow"></div> -->
          <el-menu-item index="/" route>首页</el-menu-item>
          <el-menu-item index="/about">哈啰业务</el-menu-item>
          <el-menu-item index="/about">哈啰科技</el-menu-item>
          <el-menu-item index="/about">咨询中心</el-menu-item>
          <el-menu-item index="/about">关于我们</el-menu-item>
          <el-menu-item index="/about">联系我们</el-menu-item>
        </el-menu>
      </div>


    </div>

  </header>
  <router-view />




</template>

<script lang="ts" setup>
import { ref } from "vue";
import { onMounted } from 'vue'


const isCollapse = ref(false);
const isCollapse1 = ref(false);
const collapse = () => {
  if (!isCollapse.value) {
    document.body.style.overflow = 'hidden';
  } else {
    document.body.style.overflow = 'initial';
  }
  isCollapse.value = !isCollapse.value;
}

onMounted(() => {
  isCollapse1.value = document.documentElement.clientWidth < 992;
  window.addEventListener('resize', (ev) => {
    // console.log(document.documentElement.clientWidth)
    document.body.style.overflow = 'initial';
    isCollapse1.value = document.documentElement.clientWidth < 992;
  })
})

</script>

<style lang="less" scoped>
.header {
  position: fixed;
  top: 0;
  z-index: 11;
  transition: all .6s cubic-bezier(.51, .01, 0, 1);
  width: 100%;
}

.container {
  display: flex;
  height: 80px;
  width: 992px;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
}

.left-header {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  height: 80px;
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

.collapse-button {
  display: none;
  background-color: transparent;
  border: 1px solid #fff;
  cursor: pointer;
}

.icon-bar {
  background: #fff;
  height: 2px;
  margin: 6px;
  width: 26px;
  display: block;
}

.flex-grow {
  flex-grow: 1;
}

@media screen and (max-width: 992px) {
  .header {
    width: 100%;
  }

  .container {
    width: 100%;
  }

  .right-header {
    display: none;
  }

  .collapse-button {
    display: block;
  }
}

.c-container {
  flex-direction: column;
  height: 100vh;
  justify-content: flex-start;
}

.c-right-header {
  display: block;
}

.c-el-menu-demo {
  flex-direction: column;
}
</style>
