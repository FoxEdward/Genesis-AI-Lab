<template>
  <div>
    <ul class="headerList">
      <li v-for="(item, index) in HeaderListInfo" :key="index">
        <router-link :to="item.path" class="headerListLink">
          <span>title</span>
          <el-image :src="item.img" fit="fill" style="width: 130px; height: 130px"></el-image>
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
const props = defineProps({
  HeaderListInfo: {
    type: Array<any>,
    default: true
  }
})
</script>
<style scoped>
ul {
  list-style: none;
  padding: 0;
}
.headerListLink {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 10vw;
  margin: 0 .2vw;
}
.headerList {
  display: flex;
  justify-content: space-around;
}
</style>
