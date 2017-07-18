<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello name="rod"></hello>
    <!-- <router-view></router-view> -->
  </div>
</template>

<script lang="ts">
import hello from '@/components/Hello.vue'
import { Component, Inject, Model, Prop, Provide, Vue, Watch } from 'vue-property-decorator'

@Component({
  name: 'App',
  components: {
    hello
  }
})
export default class App extends Vue {

}
// export default {
//   name: 'app',
//   components: {
//     hello,
//   }
// }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
