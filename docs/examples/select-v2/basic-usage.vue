<template>
  <el-select-v2
    v-model="value"
    :options="options"
    placeholder="Please select"
    size="large"
  />
  <el-select-v2
    v-model="value"
    :options="options"
    placeholder="Please select"
  />
  <el-select-v2
    v-model="value"
    :options="options"
    placeholder="Please select"
    size="small"
  />
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const value = ref('')
const options = Array.from({ length: 1000 }).map((_, idx) => ({
  value: `Option ${idx + 1}`,
  label: `${initials[idx % 10]}${idx}`,
}))
const initials = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
</script>

<style scoped>
.example-showcase .el-select-v2 {
  margin-right: 20px;
}
</style>
