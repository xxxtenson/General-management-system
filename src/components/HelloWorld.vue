<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <h2>{{ msg }}</h2>
  <el-button @click="count++">count is {{ count }}</el-button>
</template>

<style scoped>

</style>
