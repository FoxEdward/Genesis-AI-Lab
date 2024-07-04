<template>
  <el-container>
    <el-header>
      <el-menu default-active="1" mode="horizontal" @open="handleOpen" @close="handleClose">
        <RouterLink to="/">
          <el-menu-item index="1">
            <span>首页</span>
          </el-menu-item>
        </RouterLink>
        <router-link to="/JoinUs">
          <el-menu-item index="2">
            <span>加入我们</span>
          </el-menu-item>
        </router-link>
        <router-link to="/JoinUs">
          <el-menu-item index="2">
            <span>加入我们</span>
          </el-menu-item>
        </router-link>
        <router-link to="/JoinUs">
          <el-menu-item index="2">
            <span>加入我们</span>
          </el-menu-item>
        </router-link>
        <router-link to="/JoinUs">
          <el-menu-item index="2">
            <span>加入我们</span>
          </el-menu-item>
        </router-link>
        <router-link to="/JoinUs">
          <el-menu-item index="2">
            <span>加入我们</span>
          </el-menu-item>
        </router-link>
      </el-menu>
    </el-header>
    <el-main> <RouterView /></el-main>
  </el-container>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>

<style scoped>
.el-header {
  padding: 0;
  width: 100%;
  margin-bottom: 2vh;
}
.el-main {
  padding: 0 10vw;
}
.el-menu {
  padding-left: 9vw;
}
</style>
