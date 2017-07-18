<template>
  <div>
    <p>your name</p>
    <input v-model="msg">
    <p>prop: {{name}}</p>
    <p>msg: {{msg}}</p>
    <p>helloMsg: {{helloMsg}}</p>
    <p>computed msg: {{computedMsg}}</p>
    <button @click="greet">Greet</button>
  </div>
</template>

<script lang="ts">
import { Component, Inject, Model, Prop, Provide, Vue, Watch } from 'vue-property-decorator'

@Component
export default class Hello extends Vue {
  // prop decorator by vue-property-decorator
  @Prop()
  name: String

  // provide data (initial data)
  @Provide() msg = 123

  // use prop values for initial data
  @Provide() helloMsg = 'Hello, ' + this.msg

  // lifecycle hook
  mounted() {
    this.welecomeFn()
  }

  // computed
  get computedMsg() {
    return 'computed ' + this.msg
  }

  // method
  greet() {
    alert('greeting: ' + this.msg)
  }

  welecomeFn() {
    console.log('Welecome Typescript World')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
