<script setup lang="ts">
import { ref } from "vue";
const value = ref("");

const options = [
  {
    value: "1",
    label: "简体中文",
  },
  {
    value: "2",
    label: "繁体中文",
  },
  {
    value: "3",
    label: "English",
  },

  {
    value: "4",
    label: "にっぽん",
  },
  {
    value: "5",
    label: "한국어",
  },
  {
    value: "6",
    label: "En français",
  },
  {
    value: "7",
    label: "Das ist Deutsch.",
  },
];
</script>
<template>
 <div>
            <el-select
              v-model="value"
              class="m-2"
              placeholder="Language"
              size="large"
            >
              <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value"
              />
            </el-select>
          </div>
</template>
<style scoped>
</style>