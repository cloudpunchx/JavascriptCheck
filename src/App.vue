<template>
  <div id="app">
    <ScriptExample/>
  </div>
</template>

<script>
import ScriptExample from '@/components/ScriptExample.vue';

export default {
  name: 'App',
  components: {
    ScriptExample,
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
