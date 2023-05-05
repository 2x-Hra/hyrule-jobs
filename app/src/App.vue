<template>
  <div class="app">
    Hello
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue';


export default defineComponent({
  name: 'App',
  components: {
    
  },
  setup(){
      const state = reactive({
        
      })
    }
});
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
