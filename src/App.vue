<template>
  <div id="app">
   Parent counter : {{ $store.state.counter }} <br>
   <button @click="addCounter">+</button>
   <button @click="subCounter">-</button>

   <child></child>
  </div>
</template>

<script>
import Child from "./Child.vue";


export default {
  components:{
    child:Child
  },
  methods:{
    //이벤트 추가
    addCounter(){
      this.$store.state.counter++;
    },
    subCounter(){
      this.$store.state.counter--;
    }
  }
}
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

h1, h2 {
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
