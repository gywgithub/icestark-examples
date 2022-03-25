<script lang="ts">
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
  }
})

</script>

<template>
  <div>
    <h1>{{ msg || 'Hello Vite + icestark + Vue3!' }}</h1>
  </div>

</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
