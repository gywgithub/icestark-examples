<script lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import appHistory from '@ice/stark-app/lib/appHistory';
import { store, event } from '@ice/stark-data'
const userInfo = store.get('user');
console.log('userInfo: ', userInfo)

// const jumpToLayout = () => {
//   console.log('1111')
//   appHistory.push('/react');
// };

setTimeout(() => {
  event.emit('freshMessage', 'vue message')
}, 1000)

import { defineComponent } from 'vue'

export default defineComponent({
  // type inference enabled
  props: {
  },
  data() {
    return {
    }
  },
  mounted() {

  },
  methods: {
    jumpToLayout() {
      console.log(1333)
      appHistory.push('/react');
    }
  }
})

</script>

<template>
  <div class="wrapper">
    <img alt="Vue logo" src="https://gw.alicdn.com/imgextra/i2/O1CN01y9FKOg1f0OnH6Hew8_!!6000000003944-2-tps-200-200.png" />

    <br />
    <router-link to="/"> Home </router-link>
    <br />
    <router-link to="/list"> List </router-link>
    <br />
    <button @click="jumpToLayout">微应用间跳转</button>

    <router-view />
  </div>

</template>

<style scoped>
.wrapper {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
