<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <FormComp :msg="name" v-loading="loading"/>
  <el-button>好玩的</el-button>
</template>

<script>
import FormComp from './components/FormComp.vue'

export default {
  name: 'App',
  components: {
    FormComp
  },
  data() {
    return {     
      name: 'Vue 3',
      loading: true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
