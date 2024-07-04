<template>
  <div class="newsList demo-collapse">
    <el-collapse v-model="activeName" accordion>
      <el-collapse-item v-for="(item, index) in ListInfo" :key="index" :name="index">
        <template v-slot:title>
          <router-link to="/JoinUs">
            {{ item.title }}
          </router-link>
        </template>
        <div>{{ item.content }}</div>
      </el-collapse-item>
    </el-collapse>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
const activeName = ref('1')

const props = defineProps({
  ListInfo: {
    type: Array<any>,
    default: true
  }
})
</script>

<style scoped>

</style>
