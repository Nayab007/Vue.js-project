<template>
   <buttons/>
  <HelloWorld />
  
</template>

<script>
import buttons from './components/buttons.vue'
import HelloWorld from './components/HelloWorld.vue'


export default {
  name: 'App',
  components: {
    buttons,
    HelloWorld,
    
  
},
 
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
  margin-left: 10vw;
}
</style>
