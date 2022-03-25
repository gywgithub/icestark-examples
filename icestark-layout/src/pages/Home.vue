<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()

const innerJump = () => {
  router.push('/about')
};

const outerJump = () => {
  router.push('/seller')
}

const vueJump = () => {
  router.push({
    path: '/vue'
  })
}

</script>

<template>
  <div class="home">
    Home page

    <p><el-link type="primary" @click="innerJump">About</el-link></p>
    <p><el-link type="primary" @click="outerJump">Seller</el-link></p>
    <!-- <div>跳转到Vue子应用</div>
    <p><el-link type="primary" @click="vueJump">Vue 子应用首页</el-link></p> -->


  </div>
</template>
