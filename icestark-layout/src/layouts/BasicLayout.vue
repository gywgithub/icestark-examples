<script setup lang="ts">
import {
  Location, SetUp,
} from '@element-plus/icons-vue';
import { useRouter, useRoute } from 'vue-router';
import { computed } from 'vue';

const router = useRouter();
const route = useRoute();

const value = computed(() => {
  return route.path;
});

const handleSelect = (key: string) => {
  router.push(key);
};

</script>

<template>
  <div class="menu">
    <el-menu
      :default-active="value"
      class="el-menu-vertical-demo"
      @select="handleSelect"
      background-color="#FFF"
      text-color="black"
      active-text-color="#1989fa"
      :style="{ height: '100%', boxShadow: '0px 1px 3px 0px rgb(0 0 0 / 12%)' }"
    >
      <el-menu-item index="/">
        <template #title>
          <el-icon><location /></el-icon>
          <span>Home</span>
        </template>

      </el-menu-item>
      <el-menu-item index="/about">
        <template #title>
          <span>About</span>
        </template>

      </el-menu-item>
      <el-menu-item index="/login">
        <template #title>
          <span>Login</span>
        </template>

      </el-menu-item>

      <el-sub-menu index="/react">
        <template #title>
          <span>React 子应用</span>
        </template>

        <el-menu-item index="/react">React 子应用首页</el-menu-item>
      </el-sub-menu>

      <el-sub-menu index="/vue">
        <template #title>
          <span>Vue 子应用</span>
        </template>
        <el-menu-item index="/vue">Vue 子应用首页</el-menu-item>
      </el-sub-menu>
    </el-menu>
  </div>
</template>


<style lang="css" scoped>
.menu {
  height: 100%;
  width: 200px;
}
</style>
