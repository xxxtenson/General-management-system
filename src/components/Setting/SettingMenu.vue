<script setup lang="ts">
import {  Setting, SwitchButton } from "@element-plus/icons-vue";
import { ref } from "vue";
// import SettingTimeVue from "./SettingTime.vue";
// import SettingDarkVue from "./SettingDark.vue";
// import SettingLanguageVue from "./SettingLanguage.vue";

const centerDialogVisible = ref(false);



</script>

<template>
  <el-menu class="SettingMenu" type="Edit">
    <el-menu-item
      text
      @click="centerDialogVisible = true"
      :icon="Setting"
      circle
    >
      <el-Icon><Setting /></el-Icon>
    </el-menu-item>
  </el-menu>

  <el-dialog
    v-model="centerDialogVisible"
    width="10%"
    align-center
    :show-Close="false"
    style="border-radius: 25px; width: 50%; height: 50%"
  >
    <template #footer>
      <span class="dialog-footer">
        <div class="Changer">
          <div>Time</div>
          <SettingTime />
        </div>
        <div class="Changer">
          <div class="Changera">Language</div>
          <SettingLanguage/>
        </div>

        <div class="Changer">
          <div class="Changera"><span>Color theme change</span></div>
          <div>
            <SettingDark/>
          </div>
        </div>
        <el-button
          @click="centerDialogVisible = false"
          :icon="SwitchButton"
          class="ButtonDialog"
          :plain="true"
          round
        />
      </span>
    </template>
  </el-dialog>
</template>

<style scoped>
.SettingMenu {
  /* position: fixed; */
  bottom: 0;
  background-color: transparent;
  width: 65px;
}
.SettingDialog {
  border-radius: 50px;
}

.ButtonDialog {
  background-color: #ffdbc5;
}
.Changer {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  font-size: 20px;
  line-height: 50px;
}

</style>
