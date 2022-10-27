<script lang="ts" setup>
import { ref } from "vue";
import {
  House,
  Files,
  FolderOpened,
  Memo,
  Message,
  Checked,
  Edit,
  Comment,
} from "@element-plus/icons-vue";



const isCollapse = ref(true);
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>
<template>
  <el-menu
    default-active="1"
    class="el-menu-vertical-demo"
    :collapse="isCollapse"
    @open="handleOpen"
    @close="handleClose"
    router
  >
    <el-menu-item index="/" type="Edit">
      <el-icon><House /></el-icon>
      <template #title>首页</template>
    </el-menu-item>
    <el-menu-item index="/content" type="Edit">
      <el-icon><Files /></el-icon>
      <template #title>内容管理</template>
    </el-menu-item>
    <el-menu-item index="/material" type="Edit">
      <el-icon><FolderOpened /></el-icon>
      <template #title>素材管理</template>
    </el-menu-item>
    <el-menu-item index="/release" type="Edit">
      <el-icon><Memo /></el-icon>
      <template #title>发布文章</template>
    </el-menu-item>
    <el-menu-item index="/Comments" type="Edit">
      <el-icon><Comment /></el-icon>
      <template #title>评论管理</template>
    </el-menu-item>
    <el-menu-item index="/fans" type="Edit">
      <el-icon><Message /></el-icon>
      <template #title>粉丝管理</template>
    </el-menu-item>
    <el-menu-item index="/Trading" type="Edit">
      <el-icon><Checked /></el-icon>
      <template #title>交易数据</template>
    </el-menu-item>
    <el-menu-item>
      <a
        class="Edit"
        link
        rel="stylesheet"
        href="https://github.com/xxxtenson/General-management-system"
      >
        <el-icon><Edit /></el-icon>
      </a>
      <template #title>项目描述</template>
    </el-menu-item>
  </el-menu>

</template>

<style scoped>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
.el-menu-vertical-demo {
  background-color: transparent;
}
.Edit {
  color: #4a403a;
}
</style>
