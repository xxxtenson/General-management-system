<script setup lang="ts">
import { ref } from "vue";
const dat = ref(new Date());
const getHours = ref(dat.value.getHours());
const getMinutes = ref(dat.value.getMinutes());
const getSeconds = ref(dat.value.getSeconds());
setInterval(() => {
  //秒
  if (getSeconds.value == 59) {
    getSeconds.value = 0;
    //分
    if (getMinutes.value == 59) {
      getMinutes.value = 0;
      //时
      if (getHours.value == 23) {
        getHours.value = 0;
      } else {
        getHours.value += 1;
      }
    } else {
      getMinutes.value += 1;
    }
  } else {
    getSeconds.value += 1;
  }
}, 1000);
</script>
<template>
   <div class="Clock">
            {{ getHours }}:{{ getMinutes }}:{{ getSeconds }}
          </div>
</template>
<style scoped>
</style>