<template>
  <div class="container">
    <div class="header">
      <el-image class="img" :src="url" fit="fill" />
      <h2>AI Lab</h2>
    </div>
    <el-divider />
    <div class="main">
      <div class="left">
        <el-carousel height="50vh" width="10vw">
          <el-carousel-item v-for="item in 4" :key="item">
            <h3 class="small justify-center" text="2xl">{{ item }}</h3>
          </el-carousel-item>
        </el-carousel>
        <HeaderList :HeaderListInfo="HeaderListInfo" class="headerList" />
        <div>
          <h1>简介</h1>
          <el-divider />
          sss
        </div>
      </div>
      <div class="right">
        <h3>最新消息</h3>
        <NewsList :ListInfo="ListInfo" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import NewsList from '@/components/NewsList.vue'
import HeaderList from '@/components/HeaderList.vue'
const url = 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg'

const ListInfo = [
  {
    title: 'AI Lab',
    content: 'AI Lab',
    date: '2022-01-01',
    url: 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg'
  },
  {
    title: 'AI Lab',
    content: 'AI Lab'
  }
]
const HeaderListInfo = [{}, {}, {}, {}, {}]
</script>

<style scoped>
.header {
  display: flex;
}
.img {
  width: 130px;
  height: 130px;
  margin-right: 2vw;
}
.container {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 90%;
}
.el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.el-divider {
  margin: 1.5vh 0 3vh 0;
}
.main {
  display: flex;
  width: 100%;
}
.left {
  width: 80%;
  margin-right: 2vw;
}
.headerList {
  margin: 2vh 0;
}
.right {
  width: 20%;
}
</style>
