<script setup lang="ts">
import Menu from "./components/Menu.vue"
import SettingMenu from "./components/Setting/SettingMenu.vue";
</script>

<template>
  <el-container>
    <el-header>Header</el-header>
  
  <el-container>
    <el-aside width="64px"> <Menu></Menu>
      <SettingMenu /></el-aside>
    <el-main><router-view></router-view></el-main>
      
  </el-container>
  <el-footer>Footer</el-footer>
</el-container>
</template>

<style scoped>
.el-container {
  height: 100%;
}

.el-header {
  background-color: #4a403a;
  color: #333;
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.el-footer {
  background-color: #ef6652;
  color: #333;
  display: flex;
  align-items: center;
  font-size: 18px;
  justify-content: center;
  height: 50px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  /* background-color: rgb(87, 55, 55); */
}
.el-aside::-webkit-scrollbar {
  display: none;
}

.el-main {
  /* background-color: #e4e1e1; */
  background-color: black;
  color: #333;
  text-align: center;
}

.el-menu {
  background-color: #d3dce6;
}
</style>
