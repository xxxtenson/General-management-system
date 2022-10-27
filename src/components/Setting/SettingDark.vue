<script setup lang="ts">
import { Moon,  Sunny, } from "@element-plus/icons-vue";
import { ElMessage } from "element-plus";
import { ref } from "vue";


const value1 = ref(true);
const open = () => {
  ElMessage({
    message: "The color theme was changed successfully   🚀 🚀",
    type: "success",
  });
};
</script>
<template>

 <el-switch
              v-model="value1"
              class="ml-2"
              :active-icon="Moon"
              :inactive-icon="Sunny"
              @click="open"
              size="large"
              inline-prompt
              style="
                --el-switch-on-color: #7d7474;
                --el-switch-off-color: #aa530e;
              "
            />

</template>

<style scoped>
</style>